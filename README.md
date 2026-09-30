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
© Overture Maps Foundation contributors. Some of those names come from
Foursquare Open Source Places, licensed under the Apache License 2.0
(https://www.apache.org/licenses/LICENSE-2.0).

## Course names (2026-09-29)

Every course carries a real name or an honest label. Names come from OpenStreetMap
tags, then Overture Places (only when one candidate is unambiguous within 400 m),
then the earlier US naming run. Courses with none of those read "Golf course near
<town>". Unnamed extra courses at a facility get a plain descriptor such as
"9-hole course (par 36)". A raw OpenStreetMap id is never used as a name.

## Stroke index (2026-09-28)

Each course carries an optional `strokeIndexSourceRaw`: `"osm"` when the mappers'
`handicap` tags form a valid scorecard ranking, `"card"` when stamped from a
published scorecard, `"default"` when neither is available. With `"default"`
every hole's `handicap` is `0`, meaning "no stroke index", never a guessed ranking.
Courses with no hole routing in OSM ship as distances-only (`mappingRaw:
"distancesOnly"`); guessed routing is never published. Hole ways that OpenStreetMap draws without a
number are numbered from the course's walk order (a named group such as "Blue 3",
or the nearest next hole with a clear margin).

## Coverage (2026-09-29)

US and Great Britain, plus Canada, Germany, Australia, France, New Zealand,
Ireland, the Netherlands, Sweden, Spain, Denmark, Japan, Finland, Switzerland,
Austria, Norway, Italy, South Africa, Belgium, Portugal and South Korea —
compiled from Geofabrik country extracts of OpenStreetMap. Packs over 300 KB
that were never hosted before are held until the compact pack format ships.
