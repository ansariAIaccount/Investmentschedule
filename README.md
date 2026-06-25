# Schedule of Investments

Schedule-of-investments dashboards for Benchmark Fund 1 & 2, sourced from Investran SmartViews.

## Files

- **`live-schedule-of-investments.html`** — Live dashboard. Re-queries Investran on each open
  (runs inside Cowork via `window.cowork.callMcpTool`). Pulls holdings/cost/fair value/IRR from
  Report Wizard report **33473** ("Cost, Book, Multiple and IRR by Deal") and first-cashflow
  investment dates from report **33484** ("IRR Cash Flows"). Sortable holdings table, summary
  tiles, fund filter, and a "refreshed" timestamp.
- **`schedule-of-investments.html`** — Static React snapshot (as of 2026-03-31). Opens standalone
  in any browser; data is embedded.

## Metric definitions

- **Cost** = Cost, Current
- **Fair Value** = Market Value
- **Gross IRR** = report IRR @ Market Value (per fund: report subtotal; "All funds": pooled XIRR
  over both funds' cashflows plus terminal market value)
- **MOIC** = Fair Value ÷ Cost
- Null and zero-value positions are excluded.

## Source

Investran (FIS) — Report Wizard report 33473, folder *Direct Investments*. Tenant:
`investranweb-livedev-us.fiscloudservices.com`.
