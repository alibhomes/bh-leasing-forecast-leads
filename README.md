# betterhomes — Leads to Lease Forecast (Team Edition)

A streamlined tool for planning leasing lead volume across a mixed-unit portfolio
(apartments, townhouses, villas). This is the simplified, team-facing version.

**Two tabs**
1. **Leads by Unit Type** — recent leads generated + average leads to close, by bedroom
2. **Forecast Calculator** — enter a scenario's unit mix + timeline → leads needed, in total and per month

The calculator also lets users save scenarios in their browser and create a printable
PDF summary for the current forecast or any saved scenario.

> The full internal version (with lead-source breakdowns, portfolio overview and
> source analysis) is maintained in a separate private repo.

## Data source
All figures derive from the `Sheet4` tab of *betterhomes Leasing Inquiries.xlsx*:
**30,785 leads in the past 6 months.** Re-baseline
the close rates each quarter against fresh closed data, and keep a sensible buffer in the plan.

## How to update
Everything (data, styling, logic) lives in `index.html`. To change figures or labels, edit
the `SEG` and `COPY` blocks in the `<script>` section, then commit and push — Vercel
redeploys automatically.

```bash
git add index.html
git commit -m "Update leasing figures"
git push
```

> Confidential — for internal betterhomes leasing planning.
