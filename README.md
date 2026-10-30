# Daniel Armstrong

**Senior GIS professional — ~30 years from tactical GPS systems to enterprise geospatial platforms.**
Esri stack (ArcGIS Pro, Online, Enterprise) · Python (ArcPy, ArcGIS API for Python, pandas/NumPy/GeoPandas) · PostgreSQL/PostGIS · Terraform · GitHub Actions

I build geospatial systems that survive contact with production: pipelines that refuse to
load bad data, toolboxes with test suites, databases whose design decisions are written
down, and scheduled jobs that fail loudly instead of truncating quietly.

## What to look at

| Repo | What it shows |
|---|---|
| **[geo-etl-pipeline](https://github.com/USERNAME/geo-etl-pipeline)** | Config-driven Python ETL framework for spatial data: declarative QA gates with abort/warn/quarantine policies, transform registry, audit logging. 30+ tests, CI on 3.11–3.13, tagged releases. |
| **[arcgis-qa-toolbox](https://github.com/USERNAME/arcgis-qa-toolbox)** | ArcGIS Pro Python Toolbox + geoprocessing service publish script, built on an arcpy-free core so the logic is fully unit-tested in CI — with an AST test that *enforces* the arcpy boundary. |
| **[agol-ops-notebooks](https://github.com/USERNAME/agol-ops-notebooks)** | ArcGIS Online hosted notebooks for content audit, scheduled layer refresh (with a shrink guard that protects production from empty upstream extracts), and hosted-layer QA. Notebooks orchestrate; a tested package decides. |
| **[postgis-enterprise-patterns](https://github.com/USERNAME/postgis-enterprise-patterns)** | Enterprise spatial database architecture as running code: migrations verified against real PostGIS in CI, behavioral smoke tests, a spatial-index benchmark with real numbers (64× on radius queries at 1M points), four ADRs, and a Terraform RDS module. |
| **[hydro-network-qc](https://github.com/USERNAME/hydro-network-qc)** | Sanitized extraction of a production tool from an ICM QC suite I built for municipal hydraulic-modeling programs (12 toolboxes, ~26k lines of client work): sewer network topology validation — orphaned/terminal/missing nodes, self-loops — before the InfoWorks ICM model build. |

A thread runs through all four: **the Esri-facing layer stays thin, the logic underneath is
tested**, and every repo's README explains the architecture decisions, not just the usage.

## Background

- GIS analysis, data engineering, and Esri application development across municipal
  water/sewer infrastructure, conservation, government, energy, and defense contexts
- Built and operate a production ArcGIS Pro tooling platform for municipal smoke-test
  and InfoWorks ICM modeling programs — 12 promoted Python Toolboxes under a versioned
  tool registry and promotion process
- ArcGIS Server administration back to the standalone-server era; enterprise geodatabase
  design on PostgreSQL/PostGIS
- U.S. Army — beta-tested tactical GPS tracking systems
- Earlier career: petroleum landman — mapping workflows where a title error costs real money
