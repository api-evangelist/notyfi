---
name: Create a Notyfi tracker and read its events
description: Create a persistent tracker from a natural-language query, then poll its deduplicated canonical event feed.
api: openapi/notyfi-openapi-original.json
operations:
  - create_tracker_api_v1_trackers_post
  - list_trackers_api_v1_trackers_get
  - get_tracker_api_v1_trackers__public_id__get
  - get_tracker_progress_api_v1_trackers__public_id__progress_get
  - list_tracker_events_api_v1_trackers__public_id__events_get
---

# Create a Notyfi tracker and read its events

Use this to stand up persistent monitoring: describe what to watch once, then read new events as they appear.

## Auth
Send a Notyfi API key on every request: `Authorization: Bearer notyfi_mk_...` (or `X-Api-Key: notyfi_mk_...`). Creating trackers requires the key's **feeds:write** scope; reading requires **read**.

## Steps
1. **Create the tracker** — `POST /api/v1/trackers` (`create_tracker`) with a JSON body describing the query (8–500 chars) and a `cadence` of `instant|hourly|daily|weekly`. `instant`/`hourly` require the Pro plan (else `402`). Pass an `Idempotency-Key` header (a UUID) so a retried create returns the same tracker instead of duplicating it — reusing the key with a different body returns `409`.
2. **Capture the `public_id`** — the response tracker id has the form `fr_...`. Address the tracker by this opaque id, never by an internal slug.
3. **Watch progress** — `GET /api/v1/trackers/{public_id}/progress` (`get_tracker_progress`) reports the tracker compiling/monitoring state; `GET /api/v1/trackers/{public_id}` (`get_tracker`) returns full detail.
4. **Read events** — `GET /api/v1/trackers/{public_id}/events` (`list_tracker_events`) returns a page of deduplicated canonical events. Page with `limit` (≤ 200, default 50) and the opaque `cursor`; follow `next_cursor` until it is null.
5. **List everything** — `GET /api/v1/trackers` (`list_trackers`) enumerates active trackers, newest first.

## Rules
- **Rate limits**: on `429`, honour `Retry-After` and the `X-RateLimit-*` headers before retrying.
- **Errors**: every 4xx/5xx returns `{ "error": { "code", "message", "request_id" } }`. A `410` (`feed_deleted`) means the tracker was archived; a foreign tracker id is indistinguishable from a missing one (`404`).
- **Pagination is cursor-based** — never assume offset paging.
