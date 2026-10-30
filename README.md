# Daniel Armstrong

**GIS Director & geospatial application engineer — 30 years, from the Army's first
tactical GPS units to cloud-hosted GIS platforms on AWS.**
Esri stack (Pro · Online · Enterprise · Experience Builder Developer Edition · ArcGIS
Maps SDK for JavaScript) · Python (ArcPy, ArcGIS API for Python, pandas/NumPy) ·
PostgreSQL/PostGIS on RDS · Terraform · GitHub Actions

I run the GIS program for a multidisciplinary civil engineering firm and still write the
code myself: custom Experience Builder widgets, ArcGIS Pro toolboxes, Python data
pipelines, and the AWS infrastructure they run on. I build geospatial systems that
survive contact with production — pipelines that refuse to load bad data, toolboxes with
test suites, databases whose design decisions are written down, and scheduled jobs that
fail loudly instead of truncating quietly.

## What to look at

| Repo | What it shows |
|---|---|
| **[geo-etl-pipeline](https://github.com/USERNAME/geo-etl-pipeline)** | Config-driven Python ETL framework for spatial data: declarative QA gates with abort/warn/quarantine policies, transform registry, audit logging. 30+ tests, CI on 3.11–3.13, tagged releases. |
| **[arcgis-qa-toolbox](https://github.com/USERNAME/arcgis-qa-toolbox)** | ArcGIS Pro Python Toolbox + geoprocessing service publish script, built on an arcpy-free core so the logic is fully unit-tested in CI — with an AST test that *enforces* the arcpy boundary. |
| **[agol-ops-notebooks](https://github.com/USERNAME/agol-ops-notebooks)** | ArcGIS Online hosted notebooks for content audit, scheduled layer refresh (with a shrink guard that protects production from empty upstream extracts), and hosted-layer QA. Notebooks orchestrate; a tested package decides. |
| **[postgis-enterprise-patterns](https://github.com/USERNAME/postgis-enterprise-patterns)** | Enterprise spatial database architecture as running code: migrations verified against real PostGIS in CI, behavioral smoke tests, a spatial-index benchmark with real numbers (64× on radius queries at 1M points), four ADRs, and a Terraform RDS module. |
| **[hydro-network-qc](https://github.com/USERNAME/hydro-network-qc)** | Sanitized extraction of a production tool from an ICM QC suite I built for municipal hydraulic-modeling programs (12 toolboxes, ~26k lines of client work): sewer network topology validation — orphaned/terminal/missing nodes, self-loops — before the InfoWorks ICM model build. |

A thread runs through all five: **the Esri-facing layer stays thin, the logic underneath
is tested**, and every repo's README explains the architecture decisions, not just the
usage.

## Production work (client-owned, so described rather than linked)

- **Municipal stormwater QA/QC platform** — custom Experience Builder (Developer
  Edition) desktop application giving crew chiefs real-time oversight of Field Maps crews across a
  ~12,000-structure, 200-mile-pipeline stormwater program, with executive dashboards
  via ArcGIS Insights
- **Sanitary sewer smoke-testing suite** — field anomaly tracking app plus the ArcGIS
  Pro tooling platform behind it: 12 promoted Python Toolboxes (~26k lines) for QC,
  InfoWorks ICM model prep, reporting, and attachment management, governed by a
  versioned tool registry and promotion process
- **Town-wide public works framework** — tiered, role-based application architecture
  tracking construction and asset inventory across every permission level
- **Hydrology tooling** — LiDAR/DEM watershed delineation, flow accumulation, and
  stormwater runoff modeling supporting engineering studies
- **Cloud platform** — AWS infrastructure supporting enterprise GIS workloads:
  provisioned with Terraform, deployed through GitHub Actions CI/CD, on
  PostgreSQL/PostGIS (Amazon RDS)

## Background

- GIS Director at a civil engineering firm serving Texas, Louisiana, and Virginia
  (2018–present); before that, 14 years running my own mapping and land-management
  consultancy for oil & gas and pipeline projects
- Early-adopter ArcGIS Online user and long-term product feedback partner to Esri
  engineering teams
- Petroleum landman roots: courthouse title research, where a mapping error costs
  real money
- U.S. Army infantry sergeant — beta-tested the Cyberwarrior 2000 GPS combat asset
  tracking system and the PLGR, the service's first tactical handheld GPS receivers
