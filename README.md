# betterhomes — Leasing Lead Forecast (Team Edition)

A streamlined tool for planning leasing lead volume across a mixed-unit portfolio
(apartments, townhouses, villas). This is the simplified, team-facing version.

**Two tabs**
1. **Leads by Unit Type** — historical leads generated + average enquiries to close, by bedroom
2. **Forecast Calculator** — enter a building's unit mix + timeline → leads required, in total and per month

> The full internal version (with lead-source breakdowns, portfolio overview and
> source analysis) is maintained in a separate private repo.

## Data source
All figures derive from the `Sheet4` tab of *betterhomes Leasing Inquiries.xlsx*:
**30,785 leads · 5,659 listings · 850 closed leases.** History-repeats model — re-baseline
the close rates each quarter against fresh closed data, and pad targets 15–25%.

## How to update
Everything (data, styling, logic) lives in `index.html`. To change figures, edit the
`SEG` and `COPY` blocks in the `<script>` section, then commit and push — Vercel redeploys
automatically.

```bash
git add index.html
git commit -m "Update leasing figures"
git push
```

> Confidential — for internal betterhomes leasing planning.
