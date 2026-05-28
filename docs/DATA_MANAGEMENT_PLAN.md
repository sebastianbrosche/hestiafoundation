# Data Management Plan — Hestia Foundation

Last updated: 2026-05-29
For EU grant compliance (Horizon Europe requires open science / data management)

---

## Summary

Hestia Foundation is committed to full open science. All research data, design files, build documentation, and monitoring data will be published under open licenses and made freely available. This plan describes how we will manage data throughout the project lifecycle.

---

## Data Types

### 1. Build Documentation
- **What:** Photos, videos, CAD files, build manuals, cost spreadsheets
- **Format:** JPG/PNG, MP4, FreeCAD/SketchUp, Markdown, CSV
- **Volume:** ~50 GB over 3 years (primarily video)
- **License:** CC BY-SA 4.0

### 2. Sensor Data (Monitoring)
- **What:** Temperature, humidity, energy, structural readings from 20+ sensors
- **Format:** CSV (raw), JSON (API), Grafana dashboards (visualisation)
- **Volume:** ~100 MB/year (text data is small)
- **License:** CC BY-SA 4.0
- **Frequency:** Every 15 minutes, 24/7, 12+ months

### 3. Structural Testing Data
- **What:** Load tests, deflection measurements, material property tests
- **Format:** CSV, PDF reports, photos
- **Volume:** ~5 GB over 3 years
- **License:** CC BY-SA 4.0

### 4. Survey and Interview Data
- **What:** Volunteer feedback, resident comfort surveys, stakeholder interviews
- **Format:** Anonymised CSV, transcript PDFs
- **Volume:** ~1 GB over 3 years
- **License:** CC BY-SA 4.0 (anonymised)
- **Privacy:** GDPR-compliant; personal data stored separately and not published

### 5. Grant and Financial Data
- **What:** Grant applications, budgets, expenditure reports, invoices
- **Format:** PDF, CSV, Markdown
- **Volume:** ~2 GB over 3 years
- **License:** Financial summaries published; detailed invoices kept private for audit

---

## Data Management Lifecycle

### Collection
- **Automated:** Sensor network logs data automatically to Raspberry Pi + cloud
- **Manual:** Build photos, survey responses, testing data collected by team
- **Standardised:** All data uses consistent formats, naming conventions, and metadata

### Storage
- **Primary:** GitHub repository (public, version-controlled)
- **Backup:** Local NAS/server + cloud backup (Backblaze or similar)
- **Raw data:** Unprocessed sensor logs kept for 5 years
- **Security:** Encrypted backups; access control for sensitive data

### Processing
- **Cleaning:** Remove sensor malfunctions, outliers, calibration errors
- **Analysis:** Statistical analysis, visualisation, comparison to benchmarks
- **Documentation:** All processing steps documented in code (Python/R scripts) and published

### Publication
- **Real-time:** Sensor dashboard updated hourly
- **Quarterly:** Reports published on GitHub + website
- **Annual:** Comprehensive dataset + analysis published
- **Final:** Complete dataset at project end, archived in Zenodo or Figshare

### Archiving
- **Duration:** All data archived for 10 years minimum (EU requirement)
- **Location:** GitHub (active) + Zenodo (permanent DOI) + local backup
- **Format:** Open formats (CSV, Markdown, PNG, MP4) to ensure long-term accessibility

---

## Open Science Practices

### Pre-registration
- Research questions and methodology published before data collection begins
- Prevents p-hacking and ensures transparency

### Open Data
- All quantitative data published in machine-readable formats (CSV, JSON)
- Metadata included (sensor location, calibration dates, known issues)
- Data dictionaries provided for all datasets

### Open Code
- All analysis scripts published on GitHub (Python, R, or Julia)
- Code commented and documented
- Reproducible: anyone can re-run our analysis and get the same results

### Open Access Publications
- All publications submitted to open-access journals or preprint servers
- APCs (Article Processing Charges) budgeted in grant applications
- Preprints on arXiv or SocArXiv before peer review

### Open Hardware
- All CAD files, assembly instructions, and material specifications published
- Bill of Materials with supplier information
- Version-controlled design iterations

---

## FAIR Principles

| Principle | How We Comply |
|-----------|---------------|
| **Findable** | All data on GitHub with clear README; Zenodo DOIs for major releases; indexed by search engines |
| **Accessible** | No registration required; no paywalls; download directly from GitHub or Zenodo |
| **Interoperable** | Open formats (CSV, Markdown, FreeCAD); standardised metadata; linked to EU vocabularies |
| **Reusable** | CC BY-SA 4.0 license; clear documentation; data dictionaries; version history |

---

## Data Quality Assurance

### During Collection
- Sensor calibration against reference standards before installation
- Weekly manual checks for sensor malfunction
- Redundant sensors at critical locations
- Photo documentation of all build stages

### During Processing
- Automated outlier detection (statistical thresholds)
- Manual review of anomalous readings
- Cross-validation between multiple sensors
- Documentation of all data cleaning decisions

### During Publication
- Peer review of analysis (if published in journal)
- Community review (GitHub issues and pull requests welcome)
- Version control (all changes tracked)
- Errata and corrections published promptly

---

## GDPR and Privacy

### Personal Data We Collect
- Volunteer names, contact details, emergency contacts
- Partner organisation contacts
- Survey respondents (anonymised before publication)

### How We Protect It
- Stored separately from open data
- Access limited to core team
- Encrypted storage
- Anonymised before any publication
- Retained only as long as necessary
- Right to deletion on request

### What We Publish
- Only anonymised, aggregated data
- No individual identifiers
- No location data that could identify individuals

---

## Roles and Responsibilities

| Role | Person | Responsibilities |
|------|--------|------------------|
| **Data Manager** | TBD / Tech lead | Overall data strategy, quality control, archiving |
| **Sensor Technician** | TBD | Sensor maintenance, data logging, troubleshooting |
| **Documentation Lead** | TBD | Build photos, videos, manuals, metadata |
| **Privacy Officer** | TBD | GDPR compliance, personal data management |
| **Repository Manager** | TBD / Sebastian | GitHub repo maintenance, releases, versioning |

---

## Budget for Data Management

| Item | Cost (€) | Notes |
|------|----------|-------|
| Sensor network + logger | 500–700 | One-time |
| Cloud storage (GitHub + backup) | 0–100/year | GitHub free for public repos |
| Zenodo / Figshare | 0 | Free for researchers |
| Data manager (part-time) | 3,000–5,000/year | If funded |
| Analysis software (R, Python) | 0 | Open-source |
| External audit (if required) | 1,000–2,000 | One-time |
| **Total (3 years)** | **€4,500–€8,800** | |

---

## Compliance Checklist

For Horizon Europe and other EU grants:

- [ ] Data management plan submitted with proposal
- [ ] Open science declaration signed
- [ ] FAIR principles documented
- [ ] GDPR compliance confirmed
- [ ] Repository chosen and configured
- [ ] Metadata standards defined
- [ ] Data manager role assigned
- [ ] Budget for data management included in grant

---

*"Day one. Begin recording everything about this one."*