# Looper course packs

Precompiled golf-course geometry packs for the Looper iOS app, generated
by Looper's Foundry compiler from OpenStreetMap data.

## Attribution

Contains information from OpenStreetMap, made available under the
Open Database License (ODbL).

© OpenStreetMap contributors — https://www.openstreetmap.org/copyright

These files are a Produced Work derived from the OpenStreetMap database.
The underlying data is licensed under the ODbL 1.0:
https://opendatacommons.org/licenses/odbl/1-0/

## Format

`pack/<osm-facility-id>.json` — an array of course objects (one per
course the facility hosts) in Looper's vendor-neutral course schema.

Place names include data from Overture Maps Foundation, licensed under
CDLA-Permissive 2.0 (https://cdla.dev/permissive-2-0/).
© Overture Maps Foundation contributors.

## Stroke index (2026-09-28)

Each course carries an optional `strokeIndexSourceRaw`: `"osm"` when the mappers'
`handicap` tags form a valid scorecard ranking, `"card"` when stamped from a
published scorecard, `"default"` when neither is available. With `"default"`
every hole's `handicap` is `0`, meaning "no stroke index", never a guessed ranking.
Courses with no hole routing in OSM ship as distances-only (`mappingRaw:
"distancesOnly"`); guessed routing is never published.
