# Home or Road

A household decision tool for Will and Megan: rent a house with a yard, buy, or take a van year — and what each does to your money and your freedom.

- **Compare plans** — every plan side by side: net worth over 30 years, the freedom point (when investments could fund a lean life), buy date and rate, cash low points, and 300 randomized market paths.
- **Build plans** — each plan is a sequence: van year or not, what work looks like after, buy on a date or when ready, switch to lean spending.
- **Buy timing** — buy now vs. later under three mortgage-rate paths, when you'd be cash-ready, and what each point of rate does to the payment.
- **Van year** — the cost of a van year under three ways back to work, where the gap comes from, trip length sensitivity.
- **Homes** — saved listings on an OpenStreetMap map with each home's cost and 10-year outlook.

## How it runs

A single `index.html` on GitHub Pages. Chart.js, Leaflet and supabase-js load from public CDNs; tiles and address lookup come from OpenStreetMap.

## Data and access

Inputs, plans and saved homes live in Supabase (`hr_plan`, `hr_homes`, `hr_places`), never in this repo. Sign-in is by emailed link, and row-level security limits every table to the emails in `hr_members`. Without signing in, the page works and saves to the current browser only.
