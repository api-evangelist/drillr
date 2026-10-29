# drillr

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

drillr is a financial data and research API for the US, China and Japan. It provides financial statements, full-text filing search, natural-language company discovery, and research signals extracted from filings, news and earnings calls. The same data is served two ways: a REST API for scripts and pipelines, and a hosted MCP server for AI agents, with every reported figure linking back to its source document.

**Areas:** Financial Data · Stocks · SEC Filings · Fundamentals · Earnings · Ownership · Corporate Events · Analyst Ratings · news-signals · MCP · Agent-Native

## drillr on APIs.io

Everything profiled for drillr is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/drillr/](https://apis.io/providers/drillr/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [drillr Data MCP Server](https://apis.io/apis/drillr/drillr-data-mcp-server/) — Hosted Streamable HTTP MCP server (drillr-data) exposing the same financial data as ~10 agent-callable tools covering discovery, filings, signals and…
- [drillr Public Data API Analyst API](https://apis.io/apis/drillr/drillr-analyst-api/) — Analyst consensus and individual rating events (US only)
- [drillr Public Data API Company API](https://apis.io/apis/drillr/drillr-company-api/) — Ticker resolution, natural-language company discovery and company profiles
- [drillr Public Data API Contract API](https://apis.io/apis/drillr/drillr-contract-api/) — The machine-readable API contract itself
- [drillr Public Data API Earnings API](https://apis.io/apis/drillr/drillr-earnings-api/) — Earnings calendar and structured earnings-call summaries
- [drillr Public Data API Events API](https://apis.io/apis/drillr/drillr-events-api/) — Corporate events: financings, deals, executive changes, corporate actions, ownership (US only)
- [drillr Public Data API Executives API](https://apis.io/apis/drillr/drillr-executives-api/) — Executive roster and annual compensation (US only)
- [drillr Public Data API Filings API](https://apis.io/apis/drillr/drillr-filings-api/) — Regulatory filing lists and full-text filing search (US, Japan, China)
- [drillr Public Data API Financials API](https://apis.io/apis/drillr/drillr-financials-api/) — The three financial statements and precomputed financial metrics
- [drillr Public Data API Ownership API](https://apis.io/apis/drillr/drillr-ownership-api/) — Insider holdings and transactions, institutional holdings (US only)
- [drillr Public Data API Prices API](https://apis.io/apis/drillr/drillr-prices-api/) — Historical bars and latest closing-price snapshots (US)
- [drillr Public Data API Signal API](https://apis.io/apis/drillr/drillr-signal-api/) — Industry inflections, enterprise AI adoption and cross-source news search

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [data](https://apis.io/servers/drillr/data/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Drillr Agentic Access](https://apis.io/agentic-access/drillr/drillr-agentic-access/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Drillr Openapi Overlay](https://apis.io/overlays/drillr/drillr-openapi-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Drillr Authentication](https://apis.io/security/drillr/drillr-authentication/)
- [Drillr Domain Security](https://apis.io/security/drillr/drillr-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Drillr Plans Pricing](https://apis.io/plans/drillr/drillr-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Drillr Rate Limits](https://apis.io/rate-limits/drillr/drillr-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://drillr.ai)
- [Documentation](https://drillr.ai/docs)
- [Getting started](https://drillr.ai/docs/quickstart)
- [API reference](https://drillr.ai/docs/api)
- [Pricing](https://drillr.ai/pricing)
- [Sign up](https://drillr.ai/signup)
- [Changelog](https://drillr.ai/changelog)
- [Terms of service](https://drillr.ai/legal/terms)
- [Privacy policy](https://drillr.ai/legal/privacy)

## API Evangelist rating

**Kin Score 52.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 71.7 |
| Contract quality | 53.8 |
| Contract governance | 18.2 |
| Operational transparency | 36.8 |
| Developer ergonomics | 58.9 |
| Access clarity | 63.2 |

**Agent readiness 52.1** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | documented (partial credit) |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | partial |
| Operation Distinctiveness | distinct |

**Regulatory alignment 28.7** — Securities & Market Data

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/drillr/](https://apis.io/providers/drillr/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for drillr: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/drillr/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
