# Daniel Armstrong

**GIS Director & geospatial application engineer with 30 years, from the Army's first
tactical GPS units to cloud-hosted GIS platforms on AWS.**
Esri stack (Pro · Online · Enterprise · Experience Builder Developer Edition · ArcGIS
Maps SDK for JavaScript) · Python (ArcPy, ArcGIS API for Python, pandas/NumPy) ·
PostgreSQL/PostGIS on RDS · Terraform · GitHub Actions

I run the GIS program for a multidisciplinary civil engineering firm and still write the
code myself: custom Experience Builder widgets, ArcGIS Pro toolboxes, Python data
pipelines, and the AWS infrastructure they run on. I build geospatial systems that
survive contact with production: pipelines that refuse to load bad data, toolboxes with
test suites, databases whose design decisions are written down, and scheduled jobs that
fail loudly instead of truncating quietly.

**Live apps: [idan-armstrong.github.io/portfolio-apps](https://idan-armstrong.github.io/portfolio-apps/)**,
built with the ArcGIS Maps SDK for JavaScript on ArcGIS Location Platform, tested and
deployed by GitHub Actions ([source](https://github.com/iDan-Armstrong/portfolio-apps)).

## What to look at

| Repo | What it shows |
|---|---|
| **[geo-etl-pipeline](https://github.com/iDan-Armstrong/geo-etl-pipeline)** | Config-driven Python ETL framework for spatial data: declarative QA gates with abort/warn/quarantine policies, transform registry, audit logging. 30+ tests, CI on 3.11–3.13, tagged releases. |
| **[arcgis-qa-toolbox](https://github.com/iDan-Armstrong/arcgis-qa-toolbox)** | ArcGIS Pro Python Toolbox + geoprocessing service publish script, built on an arcpy-free core so the logic is fully unit-tested in CI, with an AST test that *enforces* the arcpy boundary. |
| **[agol-ops-notebooks](https://github.com/iDan-Armstrong/agol-ops-notebooks)** | ArcGIS Online hosted notebooks for content audit, scheduled layer refresh (with a shrink guard that protects production from empty upstream extracts), and hosted-layer QA. Notebooks orchestrate; a tested package decides. |
| **[postgis-enterprise-patterns](https://github.com/iDan-Armstrong/postgis-enterprise-patterns)** | Enterprise spatial database architecture as running code: migrations verified against real PostGIS in CI, behavioral smoke tests, a spatial-index benchmark with real numbers (64× on radius queries at 1M points), four ADRs, and a Terraform RDS module. |
| **[rds-geodatabase-ops](https://github.com/iDan-Armstrong/rds-geodatabase-ops)** | Running an ArcGIS enterprise geodatabase on Amazon RDS for PostgreSQL: a hardened Terraform module (KMS, forced TLS, IAM auth, RDS-managed secrets, pgaudit, alarms, GovCloud-ready) and an `rdsops` CLI covering posture, health, maintenance, the Esri support matrix, blue/green upgrade plans, timed restore drills, Aurora migration plans and a multi-Region fleet view. Tested with moto and real PostGIS, so CI proves it without an AWS account. |
| **[arcgis-enterprise-ops](https://github.com/iDan-Armstrong/arcgis-enterprise-ops)** | Operations checks for ArcGIS Enterprise on the REST Administrator API (`egisops`): Server, Portal and Data Store health, services and logs, WebGISDR backup checks, and whole-stack version compatibility with an Esri upgrade plan. Standard library only, tokens kept out of URLs, and built from Esri's documentation with that stated plainly in the README. |
| **[SIMServo](https://idan-armstrong.github.io/simservo/)** ([source](https://github.com/iDan-Armstrong/simservo)) | A browser training game for GIS server administration that runs the real `rdsops` and `egisops` checks inside the page through Pyodide, so every finding a player sees comes from the tools above. 100 levels, an ArcGIS Enterprise 12.1 upgrade campaign, an Aurora migration for a GovCloud client, and a fleet to run. |

A thread runs through all seven: **the Esri-facing layer stays thin, the logic underneath
is tested**, and every repo's README explains the architecture decisions, not just the
usage.

## Production work (client-owned, so described rather than linked)

- **Municipal stormwater QA/QC platform**: custom Experience Builder (Developer
  Edition) desktop application giving crew chiefs real-time oversight of Field Maps crews across a
  ~12,000-structure, 200-mile-pipeline stormwater program, with executive dashboards
  via ArcGIS Insights
- **Sanitary sewer smoke-testing suite**: field anomaly tracking app plus the ArcGIS
  Pro tooling platform behind it: 12 promoted Python Toolboxes (~26k lines) for QC,
  InfoWorks ICM model prep, reporting, and attachment management, governed by a
  versioned tool registry and promotion process
- **Town-wide public works framework**: tiered, role-based application architecture
  tracking construction and asset inventory across every permission level
- **Hydrology tooling**: LiDAR/DEM watershed delineation, flow accumulation, and
  stormwater runoff modeling supporting engineering studies
- **Cloud platform**: AWS infrastructure supporting enterprise GIS workloads:
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
- U.S. Army infantry sergeant who beta-tested the Cyberwarrior 2000 GPS combat asset
  tracking system and the PLGR, the service's first tactical handheld GPS receivers
