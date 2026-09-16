[README.md](https://github.com/user-attachments/files/32284950/README.md)
# LooHK

Phone-first map of Hong Kong public toilets, official MTR station toilets, and major malls.

Not a layer inside the Google Maps app. This is its own map. **Walk there** opens Google Maps walking directions.

## What’s in v1

- 807 FEHD public toilets
- 65 official MTR station toilets (paid / unpaid in the hint)
- 25 public bathhouses
- 32 major malls (building pin, not a cubicle; baby room marked “likely”)
- 40 currently marked suspended from FEHD remarks (hidden by “Open now”)
- Accessible flag from the FEHD map site where it exists

Not in v1: LCSD parks, portable toilets, user accounts.
Mall hours are a typical 10:00–22:30 guess. Confirm baby rooms on the mall directory.

## Run it

Needs a local web server so the data file and location API work.

```bash
cd hk-toilet-app
python3 -m http.server 8080
```

Open http://localhost:8080 on your phone (same Wi‑Fi) or laptop. Allow location.

On iPhone: Safari → Share → Add to Home Screen.

## Data

`data/toilets-v1.geojson` is generated from the research pack.
Sources: FEHD / DATA.GOV.HK, official MTR toilet page, NearbyToilet mall pins.
MTR and mall pins are building/station centroids — read the hint.

## Next

- Exact baby-care floors for each mall
- Structured “closed / wrong place / baby room” reports
- Chinese UI toggle
