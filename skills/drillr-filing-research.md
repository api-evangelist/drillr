---
name: drillr-filing-research
description: Find a company's filings and search their full text for a specific fact or disclosure in drillr.
api: drillr REST API
operations:
  - publicDataV2Tickers
  - publicDataV2Filings
  - publicDataV2FilingSearch
  - publicDataV2NewsSearch
generated: '2026-09-14'
method: generated
source: openapi/drillr-openapi.json
---

# drillr: filing research

Discover which filings exist for a company, then search their text for the fact you
need. Base URL `https://gateway.drillr.ai/api/v2`, `X-API-KEY` header.

## Steps

1. **Resolve the ticker** with `publicDataV2Tickers` (`GET /api/v2/tickers?query=`)
   if you have a name rather than a symbol.
2. **List filings** with `publicDataV2Filings` (`GET /api/v2/filings?ticker=<t>`).
   Each row carries `form_type`, `filing_date`, `period_of_report`,
   `accession_number` and a `filing_url` deep link to the official document,
   newest first. Use this to see what exists before searching content.
3. **Search filing text** with `publicDataV2FilingSearch`
   (`GET /api/v2/filing-search?ticker=<t>&query=<free text>`). Returns matching
   passages as filed, each with its `section`, `form_type`, `filing_date`,
   `language` (English/Chinese/Japanese) and a relevance `score`. This indexes the
   full text of filings, not a fixed set of line items — any figure a company ever
   filed is findable, linked to the passage it appears in.
4. **Cross-reference news** (optional) with `publicDataV2NewsSearch`
   (`POST /api/v2/news-search`, JSON body) for storylines, events and attributed
   claims around the same company or theme.

## Rules

- `filing-search` requires a resolved `ticker`; searches one company at a time.
- Coverage: US, Japan, Hong Kong, China A-shares (news + filing coverage vary by
  market). Out-of-coverage tickers return `404 not_found`.
- Respect the `{ error, message }` envelope and the 100 req/key/min rate limit;
  `429` is not billed. See `errors/` and `rate-limits/`.
