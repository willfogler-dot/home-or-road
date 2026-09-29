# Home or Road

A household planning dashboard: keep renting, buy a house, or take a van-life sabbatical, projected month by month over 10 years.

- **Summary, Rent, Buy, Van Life tabs** — net worth, cash runway, investment accounts, downside and upside cases, sensitivity grids.
- **Homes** — saved listings on an OpenStreetMap-based map with each home's monthly cost, cash to close and 10-year outlook.
- **Assumptions** — per-person inputs for the household that sum automatically.

## How it runs

A single `index.html` served by GitHub Pages. Libraries load from public CDNs (Chart.js, Leaflet, supabase-js). Basemap tiles come from CARTO (OpenStreetMap data); address lookup uses OpenStreetMap Nominatim.

## Data and access

Plan inputs and saved homes live in Supabase (`hr_plan`, `hr_homes`, `hr_places`), never in this repo. Sign-in is by emailed link. Row-level security limits every table to the emails in `hr_members`; anyone else sees only the empty example version and nothing is shared with them. The key in the page is Supabase's publishable key, which is safe to expose.

Without signing in, the page still works and saves to the current browser only.
