# Project Nightingale — Lender control, recovery and exit plan (CreditSwan intelligence packet, v4.2)

Prepared for Manulife | Comvest Credit Partners. 17 November 2026. Confidential. For discussion.
Not legal, tax or investment advice.

This site is built from `Project-Nightingale-v4.2-Comvest.md`, the plan for Comvest (Parts A to E and
Appendices A to E). It contains no adviser terms: the Operating Mandate Proposal and everything in `PRIVATE/`
are not in this folder and must not be added to it.

## Deploy to Vercel

A static site. Nothing needs building.

    cd project-nightingale
    npx vercel --prod

Or drag the folder into a Vercel project (Framework preset: Other; no build command; output directory: the
folder itself), or copy its contents over the existing Nightingale deployment and push. The zip beside this
folder, `project-nightingale-vercel-v4.2.zip`, holds the same files.

`vercel.json` sets noindex, no-store, no-referrer and no-framing headers. Those headers do not restrict
access. The packet is confidential, so turn on Vercel Deployment Protection (password or Vercel
Authentication) before sharing the address. The files under `data/` are served with the site.

## Contents

- `index.html` — one self-contained page (fonts load from Google Fonts)
- Tabs: 01 Overview · 02 Situation · 03 Competition · 04 Strategy · 05 Control · 06 Businesses ·
  07 Operating plan · 08 Value & cash · 09 Execution · 10 Assumptions & method · 11 FAQ · 12 About CreditSwan
- 221 exhibits: 131 graphs, 80 tables and 10 other visuals. Three graphs are simulators, fifteen are
  timetables (nine of them new), four are positioning maps and five are score or sensitivity grids.
- All 90 plan tables are here, each with its plan table number in the basis line. Seventy-seven are shown
  as tables in the plan's own words. Thirteen are laid out as visuals: 1.1, 2.1, 4.2, 8.5, 9.2 and 10.2 as
  diagrams, 11.5 (the six roles) as cards, and 15.3 to 15.8 (the six timetables) as charts.
- `data/plan_tables.json` — the 90 plan tables as parsed
- `data/charts.json` — the data behind the graphs. New in 4.2: keys beginning `cm_` (Sleep Media
  competition), `cc_` (Sleep Care competition), `xp_` (execution), `st_` (strategy), `co_` (control) and
  `ov_` (the Overview's copies)
- `data/exhibit_index.json` — plan table number to exhibit number, chart key to exhibit number, and
  exhibit counts by tab

## What changed from the v4.1 packet

- **Tab 03, Competition, is new.** It is plan section 6: the field, the measures and CreditSwan's scores for
  Sleep Media and for Sleep Care, and what the rivals mean for the plan. Eight sections, 15 graphs and
  9 tables. The competition section that sat on the Situation tab has moved here.
- **Tab 04, Strategy, is new as a tab.** It gathers the ten findings, the two paths, the decision rule, the
  gate, the options set aside and the fourteen decisions, which were spread across Control and Execution.
  Exhibit 4.02 is a map of the two paths.
- **Tab 09, Execution, is rebuilt.** It is plan sections 15 to 17: five phases, nine workstreams with
  owners, the first 30 days, the sale path, the hold path, the Sleep Care exit, the contested route, the
  decision calendar, spending by month, risks and open items. Six timetables are drawn as charts. Hover a
  bar for the step, its dates and its owner.
- **The order follows the argument.** Situation, competition, strategy, control, the two businesses, the
  operating plan, value and cash, execution.
- **Headlines are plainer**, and the Assumptions tab opens with sixteen terms defined once.
- Three earlier exhibits are gone because new ones replace them: the rival table on the Situation tab
  (v4.1 exhibit 2.14) and the nineteen-week roadmap chart (v4.1 exhibits 7.04 and 1.16).
- No value, case or date has changed.

## Where this differs from the plan document

- The six timetables (plan tables 15.3 to 15.8) are drawn by day as bars and diamonds. The plan shows the
  same steps as weekly or monthly grids. Row names are shortened on a phone.
- The two score grids (plan tables 6.4 and 6.8) use short column names: AI for presence in AI answers,
  Neutral for independence from sellers, Price for cash price and Finding for the cost of finding a patient.
- The home-test price graph plots the top of each list-price range against the lowest price charged
  (plan table 6.6 gives the ranges).
- Four graphs on the Strategy and Control tabs are drawn from plan tables and are not tables in the plan:
  cash by path (4.03, from table A.5), the two paths on one calendar (4.12, from tables 15.5 and 15.6),
  the forbearance against the dated tests (5.03, from tables 4.3 and 8.2) and steps by kind of consent
  (5.15, from table 8.4). The consent grouping is CreditSwan's reading, and it is for counsel to confirm.
- Exhibit titles on tab 07 are shortened to one sentence where the plan's table title is longer. The table
  itself is the plan's, word for word.
- The simulator on tab 07 uses a straight-line fit to the recovery model: the gain is the saving times
  (1.65 times the share credited plus 0.24), less 0.53 times the one-off cost. It reproduces the three
  figures in plan table 11.9 (+$1.1M, +$0.5M, −$0.1M).
- The graph of what the 3Z floor is worth beside the saving divides yearly figures by twelve.
- In the value bridge drawn from plan table A.5, the discount and the other lenders' share are the
  differences between the table's columns.
- The cash simulator applies the plan's stresses together; the plan tests them singly and one pair.
- The assumptions keep the plan's references, N-01 to N-28.

## Checks run

Chromium at 1440px and 390px, every tab scrolled through: no console errors, no horizontal overflow, every
exhibit drawn and revealed, internal links resolve and none points to the wrong tab, deep links land on
their section at both widths, `csMotion.audit()` reports no static exhibits and no wipes, and every
assumptions block sits at the foot of its section with nothing moved at load. A script also checked that
exhibits are numbered in order on every tab, that no id repeats, that each of the 90 plan tables maps to an
exhibit, and that no adviser term appears in the page.

Exhibits by tab from the motion audit (graphs / tables): Overview 21 / 0, Situation 18 / 9,
Competition 15 / 9, Strategy 9 / 5, Control 8 / 6, Businesses 12 / 10, Operating plan 12 / 15,
Value & cash 17 / 14, Execution 13 / 10, Assumptions 3 / 5.

The new graphs and diagrams were looked at as images at 1440px, and ten of them at 390px.

**Short of the house standard.** The standard is nine graphs and nine tables on each subject tab. Strategy
has five tables and two diagrams. Control has eight graphs, six tables and one diagram. Neither tab has
more tables in the plan to show.

**Not checked.** The ink theme, the print layout, widths between 390px and 1440px, and tooltips on a touch
screen. On a phone the gate labels on the workstream chart sit close together, and the column names of the
score grids are turned to fit.
