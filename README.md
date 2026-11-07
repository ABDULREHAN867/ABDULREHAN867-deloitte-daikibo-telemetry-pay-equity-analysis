# Daikibo Industrials: IoT Telemetry & Compensation Forensic Analytics
**Deloitte Data Analytics Job Simulation** | *Completed via Forage*

https://public.tableau.com/app/profile/abdul.rehan/viz/Daikibo_Telemetry_Factory_Dashboard/DaikiboTelemetry-FactoryDowntimeAnalysis?publish=yes
---

## 📌 Project Overview
This project simulates real-world consulting engagements with **Daikibo Industrials**, covering two critical business verticals:
1. **Operational Intelligence:** Diagnosing high-frequency manufacturing downtime using nested IoT telemetry data across global plants.
2. **Forensic HR Analytics:** Investigating internal employee compensation complaints to detect structural gender pay disparity.

---

## 📊 Phase 1: Factory Telemetry & Downtime Analysis (Tableau)

### Architecture & Methodology
* **Dataset Scope:** Analyzed `160,704` telemetry records spanning 4 manufacturing plants and 9 industrial equipment categories.
* **Timestamp Normalization:** Handled Unix millisecond telemetry timestamps using custom calculated fields:
  ```tableau
  Downtime Quantification: Engineered logic to convert discrete unhealthy telemetry pings into cumulative downtime minutes:
  IF [Status] = "unhealthy" THEN 10 ELSE 0 END
  Executive Dashboard PreviewKey InsightsGeographical Risk: 87.4% of total downtime (900 of 1,030 minutes) originated exclusively from two sites: daikibo-factory-seiko (480 mins) and daikibo-shenzhen (420 mins).Equipment Bottlenecks: LaserWelder (480 mins) and LaserCutter (430 mins) accounted for over 88% of all machine failures.Failure Clustering: Failures were not distributed evenly; significant multi-hour outage spikes occurred on Day 2 (400 mins) and Day 5 (490 mins).🔗 Click here to interact with the Live Tableau Dashboard⚖️ Phase 2: Gender Pay Equality Forensic Audit (Excel)Methodology & AutomationProcessed corporate salary benchmarking data across global facilities. Created automated equality classifications based on absolute variance thresholds:ClassificationVariance RuleBusiness ContextFairScore between -10 and +10Statistically balanced salary distributionUnfairScore between 11 and 20 (or -11 and -20)Mild pay variance requiring reviewHighly DiscriminativeScore < -20 or > +20Severe institutional disparity requiring urgent interventionFormula Implemented:Excel=IF(ABS(C2)<=10, "Fair", IF(ABS(C2)<=20, "Unfair", "Highly Discriminative"))
Forensic FindingsExecutive Disparity: The highest concentrations of severe disparity (-21 to -26) were clustered in executive and managerial tiers (C-Level, VP, and Senior Management roles).Entry-Level Parity: Engineering and machine operator roles across European and Asian facilities predominantly remained within the Fair boundary range (-7 to +4).🛠️ Tools & Technologies UsedTableau Desktop Public Edition: Interactive dashboarding, calculated fields, continuous line charts, cross-filtering.Advanced Excel: Nested logical formulas (IF, ABS), categorical segmentation.JSON / Telemetry Processing: High-volume nested time-series data analysis.
Tools & Technologies Used
Tableau Desktop Public Edition: Interactive dashboarding, calculated fields, continuous line charts, cross-filtering.

Advanced Excel: Nested logical formulas (IF, ABS), categorical segmentation.

JSON / Telemetry Processing: High-volume nested time-series data analysis.
  
