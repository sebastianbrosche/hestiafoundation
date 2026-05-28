# Monitoring & Evaluation Framework — Shell A Prototype

Last updated: 2026-05-29
For 12-month performance assessment and data publication

---

## Purpose

The Shell A prototype is not just a building — it is a laboratory. For 12 months, we will collect continuous data on:
- **Thermal performance** — Does it stay comfortable without heating/cooling?
- **Structural integrity** — Does the pallet system settle, warp, or degrade?
- **Moisture management** — Does condensation or mould occur?
- **Energy use** — How much energy for lights, devices, water heating?
- **Durability** — How do pallets perform in Algarve's hot, dry, occasionally wet climate?

All data will be published open-source (CC BY-SA 4.0) on GitHub.

---

## Research Questions

### Primary Questions
1. Can a pallet-based wall assembly achieve U-values comparable to conventional timber frame construction?
2. Does the system maintain interior temperatures between 18–24°C without active heating or cooling in Algarve's climate?
3. Is there any measurable structural settlement, deflection, or degradation over 12 months?
4. Does the system prevent interstitial condensation and mould growth?
5. What is the total embodied carbon per m² compared to conventional construction?

### Secondary Questions
6. How do different insulation thicknesses affect performance?
7. What is the acoustic performance (STC rating) of pallet walls?
8. How does the system perform during Algarve's rare storm events (rain, wind)?
9. What maintenance is required in the first year?
10. How do occupants perceive thermal comfort and air quality?

---

## Sensor Network

### Sensor Placement (Minimum Viable Network)

| Location | Sensor Type | Quantity | Purpose | Cost (€) |
|----------|-------------|----------|---------|----------|
| **Exterior (north wall, shaded)** | Temperature + humidity | 1 | Ambient climate reference | 30 |
| **Exterior (south wall, sun-exposed)** | Temperature + humidity | 1 | Solar gain reference | 30 |
| **Interior (living area, centre)** | Temperature + humidity + CO₂ | 1 | Occupant comfort | 50 |
| **Interior (bed area)** | Temperature + humidity | 1 | Night-time comfort | 30 |
| **Wall cavity (north)** | Temperature + humidity | 2 | Insulation performance, condensation risk | 60 |
| **Wall cavity (south)** | Temperature + humidity | 2 | High-stress side | 60 |
| **Roof cavity** | Temperature + humidity | 2 | Roof insulation performance | 60 |
| **Floor underside** | Temperature + humidity | 1 | Ground moisture, thermal bridge | 30 |
| **Electrical panel** | Energy monitor (clamp meter) | 1 | Total energy consumption | 40 |
| **Water tank** | Temperature | 1 | Water heating energy | 20 |
| **Structural (2 corners)** | Inclinometer / tilt sensor | 2 | Settlement and racking | 80 |
| **Structural (roof beam)** | Strain gauge (optional) | 1 | Load deflection | 100 |
| **Door/window** | Open/close reed switch | 2 | Ventilation behaviour | 10 |
| **Rain gauge** | Tipping bucket | 1 | Precipitation correlation | 25 |
| **Wind** | Anemometer (optional) | 1 | Wind load correlation | 30 |

**Total sensors:** 20+ units
**Total cost:** €500–700

### Data Logger
- **Hardware:** Raspberry Pi 4 (€60) or Arduino + WiFi module (€30)
- **Storage:** Local SD card + cloud upload (GitHub, ThingSpeak, or自建InfluxDB)
- **Frequency:** Every 15 minutes (96 readings/day per sensor)
- **Backup:** Local storage if internet fails; upload when connection restored
- **Power:** USB from mains or solar battery system

---

## Data Collection Protocol

### Continuous (Automated)
- All sensor readings every 15 minutes
- Upload to cloud database every hour
- Check for sensor malfunctions daily (automated alert if readings are null or out of range)

### Weekly (Manual)
- Visual inspection of exterior and interior
- Photograph any changes, cracks, or moisture marks
- Check for pest activity (termites, rodents)
- Check for UV degradation of external materials
- Record any maintenance actions

### Monthly (Manual)
- Download and review all sensor data
- Check for anomalies or drift
- Calibrate sensors against handheld reference (thermometer, hygrometer)
- Structural check: measure any settlement at corners
- Energy bill recording (if on grid) or solar production logging
- Update maintenance log

### Quarterly (Formal)
- Comprehensive visual inspection with photos
- Thermal camera scan (if available) for cold bridges
- Moisture meter readings of wall and roof cavities
- Structural measurement: diagonal dimensions, plumb check
- Occupant comfort survey (if occupied)
- Publish quarterly data report on GitHub

### Annually (Final Assessment)
- Full structural inspection by licensed engineer
- Comprehensive sensor data analysis and report
- Comparison to Eurocode 5 design assumptions
- Embodied carbon calculation (LCA)
- Final publication: peer-reviewed paper or technical report
- Decision on system modifications for Shell B

---

## Data Publication

### Real-Time Dashboard
- URL: TBD (could be a simple webpage or Grafana instance)
- Shows: Current interior/exterior temperature, humidity, energy use
- Updates: Every hour
- Public access: Yes

### GitHub Repository
- Path: `data/monitoring/YYYY-MM/`
- Format: CSV files (one per sensor, one per month)
- Schema: `timestamp, sensor_id, location, temperature_c, humidity_pct, ...`
- License: CC BY-SA 4.0
- README: Full description of sensor placement, calibration, known issues

### Quarterly Reports
- Format: Markdown + PDF
- Contents:
  - Executive summary
  - Climate context (local weather data)
  - Thermal performance analysis
  - Moisture and condensation assessment
  - Structural observations
  - Energy performance
  - Photos and diagrams
  - Comparison to design targets
  - Recommendations for system improvement
- Publication: GitHub + website blog post + social media

### Final Report (Month 12)
- Format: Technical report (50+ pages) + peer-reviewed paper (if possible)
- Contents:
  - Full methodology
  - 12-month dataset
  - Statistical analysis
  - Structural engineering assessment
  - LCA (embodied carbon)
  - Cost analysis
  - Scalability assessment
  - Policy implications
- Publication: GitHub + submit to relevant journal (e.g., *Construction and Building Materials*, *Energy and Buildings*, or *Sustainability*)

---

## Success Criteria (KPIs)

| KPI | Target | Measurement |
|-----|--------|-------------|
| **Interior temperature comfort** | 18–24°C for >90% of hours | Temperature sensor data |
| **No condensation risk** | Dew point never reached in wall cavities | Humidity + temperature in cavities |
| **No mould growth** | Zero visible mould | Visual inspection |
| **Structural integrity** | <5mm settlement/deflection | Inclinometer + manual measurement |
| **Energy use** | <50 kWh/m²/year | Energy monitor + billing data |
| **Durability** | No material failure requiring repair | Visual inspection + maintenance log |
| **Embodied carbon** | <200 kg CO₂e/m² | LCA calculation |
| **Data completeness** | >95% uptime for all sensors | Automated logging check |
| **Open publication** | All data published within 30 days of collection | GitHub commit history |

---

## Comparison Benchmarks

| Metric | Hestia Shell A Target | Conventional Portuguese Construction | Passive House Standard |
|--------|----------------------|-------------------------------------|------------------------|
| U-value (walls) | 0.25–0.35 W/m²K | 0.35–0.50 | ≤0.15 |
| U-value (roof) | 0.20–0.30 W/m²K | 0.30–0.50 | ≤0.15 |
| U-value (floor) | 0.25–0.35 W/m²K | 0.40–0.60 | ≤0.20 |
| Air tightness | 3–5 ACH50 | 5–10 | ≤0.6 |
| Heating demand | <15 kWh/m²/year | 50–100 | ≤15 |
| Cooling demand | <15 kWh/m²/year | 30–60 | ≤15 |
| Embodied carbon | <200 kg CO₂e/m² | 300–500 | 150–300 |

Note: Hestia targets "good enough" not "best in class." The goal is affordable adequacy, not luxury performance.

---

## Risk Mitigation for Monitoring

| Risk | Mitigation |
|------|------------|
| Sensor failure | Redundant sensors at critical locations; weekly manual checks |
| Data logger failure | Local SD card backup; cloud sync every hour |
| Power outage | Battery backup for logger; solar panel if off-grid |
| Vandalism / theft | Secure enclosure; site access control; cheap sensors (<€50 each) |
| Pest damage | Regular inspection; sensor housing sealed |
| Calibration drift | Quarterly calibration against reference; record drift rates |
| Occupant interference | Clear signage; simple user guide; tamper-evident seals |

---

## Budget

| Item | Cost (€) |
|------|----------|
| Sensors (20+ units) | 500–700 |
| Data logger (Raspberry Pi / Arduino) | 60–100 |
| Cloud storage / database | 0–50/year |
| Thermal camera rental (quarterly) | 200–400 |
| Structural engineer inspection (annual) | 500–1,000 |
| LCA consultant (one-off) | 1,000–2,000 |
| Publication costs (open access fee) | 1,000–2,000 |
| **Total Year 1** | **€3,260–€6,250** |

---

## Timeline

| Phase | Date | Action |
|-------|------|--------|
| **Pre-build** | August 2026 | Order sensors, assemble logger, test network |
| **Install** | Day 10 of build | Install all sensors, calibrate, begin logging |
| **Baseline** | Month 0 | Record initial readings, confirm all sensors functional |
| **Q1 Report** | November 2026 | First quarterly report (if build complete by September) |
| **Q2 Report** | February 2027 | Winter performance in Algarve (mild, but relevant) |
| **Q3 Report** | May 2027 | Spring performance, storm season check |
| **Q4 Report** | August 2027 | Summer performance (peak heat, critical test) |
| **Final Report** | September 2027 | 12-month complete analysis and publication |

---

*"Day one. Begin recording everything about this one."*
