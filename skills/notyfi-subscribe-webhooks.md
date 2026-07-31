---
name: Subscribe to Notyfi tracker events over webhooks
description: Register an HMAC-signed webhook endpoint for tracker events, test it, and rotate its secret.
api: openapi/notyfi-openapi-original.json
operations:
  - create_webhook_endpoint_api_v1_webhooks_post
  - list_webhook_endpoints_api_v1_webhooks_get
  - update_webhook_endpoint_api_v1_webhooks__webhook_id__patch
  - test_webhook_endpoint_api_v1_webhooks__webhook_id__test_post
  - rotate_webhook_secret_api_v1_webhooks__webhook_id__rotate_secret_post
  - delete_webhook_endpoint_api_v1_webhooks__webhook_id__delete
---

# Subscribe to Notyfi tracker events over webhooks

Use this to receive tracker events by push instead of polling.

## Auth
Send a Notyfi API key (`Authorization: Bearer notyfi_mk_...` or `X-Api-Key`). Webhook mutations require the **feeds:write** scope.

## Steps
1. **Create the endpoint** — `POST /api/v1/webhooks` (`create_webhook_endpoint`) with the destination `url`, the `events` to subscribe to (`tracker.event.created`, `tracker.event.updated`), and optional `tracker_ids` (empty = every tracker the account owns). The response returns the HMAC `signing_secret` **exactly once** — store it now; it is never shown again.
2. **Verify signatures** — validate the HMAC signature on each delivery using the stored `signing_secret`. Reject unsigned or mismatched payloads.
3. **Test it** — `POST /api/v1/webhooks/{webhook_id}/test` (`test_webhook_endpoint`) sends a sample delivery so you can confirm receipt and signature verification end to end.
4. **Rotate the secret** — `POST /api/v1/webhooks/{webhook_id}/rotate-secret` (`rotate_webhook_secret`) issues a new signing_secret (returned once); update your verifier atomically.
5. **Manage** — `GET /api/v1/webhooks` (`list_webhook_endpoints`), `PATCH .../{webhook_id}` (`update_webhook_endpoint`) to change url/events/enabled, and `DELETE .../{webhook_id}` (`delete_webhook_endpoint`) to remove it.

## Rules
- **Endpoint limit**: `409` means the account reached its webhook endpoint limit.
- **Not configured**: `503` means webhook signing is not configured on the deployment.
- **Errors**: standard `{ "error": { "code", "message", "request_id" } }` envelope; on `429` honour `Retry-After`.
