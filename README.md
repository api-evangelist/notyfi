# Notyfi

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Notyfi is a natural-language monitoring and notification service built by Perceptron ML (Y Combinator). Describe what to watch in one sentence -- new lawsuits, layoffs, price drops, listings, RFPs, breaking news -- and Notyfi watches the news, filings, databases, and the open web for it, delivering deduplicated canonical events instantly, hourly, daily, or weekly by email, on a live dashboard, or into agents and workflows via a REST API and a hosted MCP server. The API exposes persistent trackers, their event feeds, HMAC-signed outgoing webhooks, API-key management, account, and Stripe-backed billing. Authenticate with a Notyfi API key (Authorization: Bearer notyfi_mk_... or X-Api-Key).

**Areas:** Company · Notification · Monitoring · Webhook · Real-Time · Agents · MCP · Alerts

## Notyfi on APIs.io

Everything profiled for Notyfi is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/notyfi/](https://apis.io/providers/notyfi/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Notyfi Account API](https://apis.io/apis/notyfi/notyfi-account-api/) — The account API from Notyfi — 3 operation(s) for account.
- [Notyfi Billing API](https://apis.io/apis/notyfi/notyfi-billing-api/) — The billing API from Notyfi — 3 operation(s) for billing.
- [Notyfi Keys API](https://apis.io/apis/notyfi/notyfi-keys-api/) — The keys API from Notyfi — 2 operation(s) for keys.
- [Notyfi Trackers API](https://apis.io/apis/notyfi/notyfi-trackers-api/) — The trackers API from Notyfi — 6 operation(s) for trackers.
- [Notyfi Webhooks API](https://apis.io/apis/notyfi/notyfi-webhooks-api/) — The webhooks API from Notyfi — 4 operation(s) for webhooks.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Notyfi Webhooks](https://apis.io/asyncapis/notyfi/notyfi-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [Notyfi](https://apis.io/servers/notyfi/notyfi/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Notyfi Agentic Access](https://apis.io/agentic-access/notyfi/notyfi-agentic-access/)

#### Collections (5)

Postman and Open Collection request collections.

- [Notyfi account API](https://apis.io/collections/notyfi/open-notyfi-account-api/)
- [Notyfi account billing API](https://apis.io/collections/notyfi/open-notyfi-billing-api/)
- [Notyfi account keys API](https://apis.io/collections/notyfi/open-notyfi-keys-api/)
- [Notyfi account trackers API](https://apis.io/collections/notyfi/open-notyfi-trackers-api/)
- [Notyfi account webhooks API](https://apis.io/collections/notyfi/open-notyfi-webhooks-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Notyfi Openapi Overlay](https://apis.io/overlays/notyfi/notyfi-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Notyfi Authentication](https://apis.io/security/notyfi/notyfi-authentication/)
- [Notyfi Domain Security](https://apis.io/security/notyfi/notyfi-domain-security/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://notyfi.com)
- [Documentation](https://notyfi.com/docs)
- [API reference](https://notyfi.com/docs)
- [Pricing](https://notyfi.com/#pricing)
- [Sign up](https://notyfi.com/dashboard/#signup)
- [Blog](https://perceptronml.com/blog/)
- [Terms of service](https://notyfi.com/terms)
- [Privacy policy](https://notyfi.com/privacy)

## API Evangelist rating

**Kin Score 25.1** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 54.0 |
| Contract governance | 4.5 |
| Operational transparency | 7.9 |
| Developer ergonomics | 16.1 |
| Access clarity | 0.0 |

**Agent readiness 34.7** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | verified |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 16.7** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/notyfi/](https://apis.io/providers/notyfi/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Notyfi: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/notyfi/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
