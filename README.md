# Project Nightingale — Lender control, recovery and exit plan (CreditSwan intelligence packet, v4.1)

Prepared for Manulife | Comvest Credit Partners. 17 November 2026. Confidential. For discussion.
Not legal, tax or investment advice.

This site is built from `Project-Nightingale-v4.1-Comvest.md`, the plan for Comvest (Parts A to E and
Appendices A to E). It contains no adviser terms: the Operating Mandate Proposal and everything in `PRIVATE/`
are not in this folder and must not be added to it.

## Deploy to Vercel

A static site. Nothing needs building.

    cd project-nightingale
    npx vercel --prod

Or drag the folder into a Vercel project (Framework preset: Other; no build command; output directory: the
folder itself), or copy its contents over the existing Nightingale deployment and push. The zip beside this
folder, `project-nightingale-vercel-v4.1.zip`, holds the same files.

`vercel.json` sets noindex, no-store, no-referrer and no-framing headers. Those headers do not restrict
access. The packet is confidential, so turn on Vercel Deployment Protection (password or Vercel
Authentication) before sharing the address. The files under `data/` are served with the site.

## Contents

- `index.html` — one self-contained page (fonts load from Google Fonts)
- Tabs: 01 Overview · 02 Situation · 03 Control · 04 Businesses · 05 Operating plan · 06 Value & cash ·
  07 Execution · 08 Assumptions & method · 09 FAQ · 10 About CreditSwan
- Tab 05, Operating plan, is the plan's sections 10.3 to 10.6 and Appendix E: how far AI can reduce the
  MediaCo team. Eight sections: team size, staffing models, the core of six, stages, the run-off, value,
  limits and supporting evidence. It has 13 graphs, one of them a simulator of Comvest's gain on a hold
  against the share of the saving a buyer pays for, and 14 tables.
- All 70 plan tables are here in the plan's own words, each with its plan table number in the basis line.
  Table 10.5 (the six roles) is laid out as cards. Seven tables from the earlier parts are also laid out as
  visuals: 1.1, 2.1, 4.2, 7.4, 7.5, 8.2 and 9.2.
- 103 graphs re-draw figures from the tables and sections; three are simulators.
- `data/plan_tables.json` — the 70 plan tables as parsed
- `data/charts.json` — the data behind the graphs (operating-plan graphs carry the prefix `op_`)
- `data/exhibit_index.json` — plan table number to exhibit number, and exhibit counts by tab

## Where this differs from the plan document

- Exhibit titles on tab 05 are shortened to one sentence where the plan's table title is longer. The table
  itself is the plan's, word for word.
- The simulator on tab 05 uses a straight-line fit to the recovery model: the gain is the saving times
  (1.65 times the share credited plus 0.24), less 0.53 times the one-off cost. It reproduces the three
  figures in plan table 10.9 (+$1.1M, +$0.5M, −$0.1M).
- The graph of what the 3Z floor is worth beside the saving divides yearly figures by twelve.
- The consent dot grid (plan table 7.4) sorts the plan's wording into four kinds of consent. The grouping
  is CreditSwan's reading, and it is for counsel to confirm.
- In the value bridge drawn from plan table A.5, the discount and the other lenders' share are the
  differences between the table's columns.
- The Competition section on tab 02 gathers the plan's rival and buyer material in one place.
- The cash simulator applies the plan's stresses together; the plan tests them singly and one pair.
- The assumptions keep the plan's references, N-01 to N-26.

## Checks run

Chromium at 1440px and 390px, every tab scrolled through: no console errors, no horizontal overflow, every
exhibit drawn and revealed, internal links resolve, deep links land on their section, `csMotion.audit()`
reports no static exhibits and no wipes, and every assumptions block sits at the foot of its section with
nothing moved at load. Exhibits by tab from the audit (graphs / tables): Overview 17 / 0, Situation 20 / 10,
Control 10 / 8, Businesses 12 / 10, Operating plan 12 / 15, Value & cash 17 / 14, Execution 9 / 8,
Assumptions 3 / 5. The new graphs were looked at as images at 1440px and three of them at 390px.
Not checked: the ink theme, print layout, and widths between 390px and 1440px. On a phone the axis labels
of a few bar charts with two-decimal money formats sit close together.
