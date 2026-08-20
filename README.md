# DR Congo Administrative Divisions / République démocratique du Congo



## Overview

| Item | Details |
|------|---------|
| Province | 26 |
| Territory | 164 |
| Sector | 519 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-08-20 |
| Website | [openadmindata.org/cd](https://openadmindata.org/cd/) |
| API | [openadmindata.org/api/cd](https://openadmindata.org/api/cd/) |
| Flag | [PNG](https://onlygames.me/flags-png/cd/) · [SVG](https://onlygames.me/flags-svg/cd/) · [PDF](https://onlygames.me/flags-pdf/cd/) |
| National Anthem | [🎵 Listen & Download DR Congo National Anthem MP3](https://onlygames.me/national-anthems/cd/) |

## Browse by Province

| # | Province | Territorys | Sectors | Link |
|---|----|----|----|------|
| 1 | Kinshasa | 1 | 35 | [Browse](divisions/kinshasa/) |
| 2 | Kongo-Central | 12 | 31 | [Browse](divisions/kongo-central/) |
| 3 | Kwango | 5 | 14 | [Browse](divisions/kwango/) |
| 4 | Kwilu | 7 | 24 | [Browse](divisions/kwilu/) |
| 5 | Maï-Ndombe | 8 | 14 | [Browse](divisions/ma-ndombe/) |
| 6 | Equateur | 8 | 18 | [Browse](divisions/equateur/) |
| 7 | Sud-Ubangi | 5 | 16 | [Browse](divisions/sud-ubangi/) |
| 8 | Nord-Ubangi | 5 | 11 | [Browse](divisions/nord-ubangi/) |
| 9 | Mongala | 3 | 12 | [Browse](divisions/mongala/) |
| 10 | Tshuapa | 6 | 12 | [Browse](divisions/tshuapa/) |
| 11 | Tshopo | 8 | 23 | [Browse](divisions/tshopo/) |
| 12 | Bas-Uele | 6 | 11 | [Browse](divisions/bas-uele/) |
| 13 | Haut-Uele | 6 | 13 | [Browse](divisions/haut-uele/) |
| 14 | Ituri | 5 | 36 | [Browse](divisions/ituri/) |
| 15 | Nord-Kivu | 9 | 34 | [Browse](divisions/nord-kivu/) |
| 16 | Sud-Kivu | 9 | 34 | [Browse](divisions/sud-kivu/) |
| 17 | Maniema | 8 | 18 | [Browse](divisions/maniema/) |
| 18 | Haut-Katanga | 8 | 28 | [Browse](divisions/haut-katanga/) |
| 19 | Lualaba | 5 | 13 | [Browse](divisions/lualaba/) |
| 20 | Haut-Lomami | 5 | 16 | [Browse](divisions/haut-lomami/) |
| 21 | Tanganyika | 6 | 11 | [Browse](divisions/tanganyika/) |
| 22 | Lomami | 6 | 16 | [Browse](divisions/lomami/) |
| 23 | Kasaï-Oriental | 6 | 19 | [Browse](divisions/kasa-oriental/) |
| 24 | Sankuru | 6 | 16 | [Browse](divisions/sankuru/) |
| 25 | Kasaï-Central | 6 | 26 | [Browse](divisions/kasa-central/) |
| 26 | Kasaï | 5 | 18 | [Browse](divisions/kasa/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-province.json](data/all-province.json) | JSON | All 26 province records |
| [all-territory.json](data/all-territory.json) | JSON | All 164 territory records |
| [all-sector.json](data/all-sector.json) | JSON | All 519 sector records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-2 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-province.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['territory']} territorys")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-province.json", "utf-8"));
console.log(`Total: ${data.length} provinces`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=province, 2=territory, 3=sector |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{province-slug}/
divisions/{province-slug}/{territory-slug}/
```

Sectors are listed inline in each territory's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-province links
- [Per-province data](docs/llms-full/) — Full data by province

## Citation

```
DR Congo Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/dr-congo-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
