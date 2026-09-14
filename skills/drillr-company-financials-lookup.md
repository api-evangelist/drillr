---
name: drillr-company-financials-lookup
description: Resolve a company name to a ticker and pull its recent financial statements from drillr.
api: drillr REST API
operations:
  - publicDataV2Tickers
  - publicDataV2CompanyProfile
  - publicDataV2IncomeStatements
  - publicDataV2BalanceSheets
  - publicDataV2CashFlowStatements
  - publicDataV2FinancialMetricsSnapshot
generated: '2026-09-14'
method: generated
source: openapi/drillr-openapi.json
---

# drillr: company financials lookup

Turn a company name into a ticker, then read its reported financials. All calls are
GET against `https://gateway.drillr.ai/api/v2` with the `X-API-KEY` header.

## Steps

1. **Resolve the ticker.** Call `publicDataV2Tickers` (`GET /api/v2/tickers`) with
   `query=<name, code, ISIN, CIK or CUSIP>` and optional `market`. One ticker keys
   both the company and its market (US bare `AAPL`, Japan `6758.T`, HK `00700.HK`,
   A-share `600519.SH`, Korea `005930.KS`). If you only have a description, use
   `publicDataV2CompanyDiscovery` (`GET /api/v2/company-discovery`) instead.
2. **(Optional) confirm the company.** Call `publicDataV2CompanyProfile`
   (`GET /api/v2/company-profile?ticker=<t>`) to verify name, exchange, sector and
   listing.
3. **Pull statements.** Call `publicDataV2IncomeStatements`,
   `publicDataV2BalanceSheets` and `publicDataV2CashFlowStatements` with
   `ticker=<t>`, optional `period` (e.g. `FY`) and `limit`. Rows come back under
   `data`, newest period first, with `period_start`, `report_period`, `currency`
   and `accounting_standard` stated explicitly — do not infer the fiscal calendar.
4. **Snapshot metrics.** For current ratios/per-share/growth, call
   `publicDataV2FinancialMetricsSnapshot` with `ticker=<t>`.

## Rules

- These endpoints are not paginated and do not filter by amount — fetch rows and
  filter client-side. Fewer rows than `limit` means fewer matching periods exist.
- Handle errors from the `{ error, message }` envelope: `404 not_found` for an
  out-of-coverage ticker, `402 insufficient_credits`, `429 rate_limit_exceeded`
  (back off using `retry_after_seconds`; not billed). See
  `errors/drillr-problem-types.yml`.
- Rate limit is 100 requests per key per minute (`rate-limits/drillr-rate-limits.yml`).
