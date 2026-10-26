# TimescaleDB Cookbook

<!-- ZQM-START -->
<!-- markdownlint-disable MD033 -->
<p align="center">
  <strong>ZQM Computing — Geospatial Engineering & Scientific Computing</strong><br>
  <a href="https://github.com/ZQM-Computing">ZQM Computing</a>
</p>
<!-- markdownlint-enable MD033 -->
<!-- ZQM-END -->

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

A **TimescaleDB cookbook** — time-series hypertables on Postgres. Honest status: files and preload are in place on Node-1, but CREATE EXTENSION retries wait on the PostgreSQL 17.11 upgrade, so extension verification is pending. Patterns are planned, not yet run on the fleet. It is intended for Engineers who store time-series sensor and observation data in Postgres. Validate each pattern against your own data, software versions, and operating environment before adopting it.

## Repository role and status

**Status:** Active, public — seeding. Pattern passes land in follow-up work from fleet-verified setups; the tables below list what is planned, not what is already written.

**What this repository is:** TimescaleDB patterns — see the table below.

**What it contributes:** Part of the ZQM Computing geospatial portfolio. The umbrella index for the series is [geospatial-cookbooks](https://github.com/ZQM-Computing/geospatial-cookbooks).

**Standing:** This repository is maintained independently. Automated checks cover only the paths and environments configured in its workflows; they do not establish production readiness or operational certification.

## Who this is for

Engineers who store time-series sensor and observation data in Postgres.

## Prerequisites

- PostgreSQL 17 with the TimescaleDB extension files
- PostGIS-backed Postgres for geo time-series passes

## Patterns (planned)

| # | Example | What it will demonstrate |
|---|---------|--------------------------|
| 01 | `01-hypertable` | Creating hypertables from timestamped tables |
| 02 | `02-compression` | Compression policies for older chunks |
| 03 | `03-continuous-aggregates` | Continuous aggregates for downsampled views |
| 04 | `04-geo-pairing` | Pairing hypertables with PostGIS geometries |

## Repository layout

```text
timescaledb-cookbook/
├── examples/          # pattern passes, landing in follow-up work
├── README.md
└── LICENSE
```

## Roadmap

- First pattern pass: the first two table rows
- Second pass: the remaining rows, from fleet-verified setups

## Contributing

A contributing guide lands with the first pattern pass. Report security issues to <zqmcomputing@gmail.com> — please do not open a public issue for those.

## More from this series

- [postgis-cookbook](https://github.com/ZQM-Computing/postgis-cookbook) — Spatial indexing, joins & KNN, SRID management, vector tiles
- [pgstac-cookbook](https://github.com/ZQM-Computing/pgstac-cookbook) — STAC catalogs in PostGIS, stac-fastapi APIs, bulk ingest
- [grafana-cookbook](https://github.com/ZQM-Computing/grafana-cookbook) — Dashboards, datasources, and alerts for geospatial stacks
