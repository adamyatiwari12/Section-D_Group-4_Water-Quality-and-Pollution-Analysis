# 🌊 River Water Quality Monitoring & Analysis Dashboard

> **Data Visualisation & Analytics** | Environment & Water Resources Analytics Project
<img width="639" height="611" alt="Screenshot 2026-02-18 at 2 05 30 PM" src="https://github.com/user-attachments/assets/c392e00a-1596-4e00-8843-d8e347f1e68e" />

---

## 🏷️ Team Identity

| Field | Details |
|-------|---------|
| **Sector** | Environment & Water Resources |
| **Institute** | Newton School of Technology |
| **Subject** | Data Visualisation & Analytics |
| **Academic Year** | 2nd Year, 4th Semester |
| **Tools Used** | Google Sheets (Pivot Tables, Calculated Columns, Charts, Slicers, Dashboard) |

---

## 👥 Team Members

| Name | Role |
|------|------|
| Adamya Tiwari | Project Lead |
| Vishuti Jamwal | PPT & Quality Lead |
| Kartik Yadav | Dashboard Lead |
| Bhavya Punj | Strategy Lead |
| Om Chimurkar | Data Lead |
| Jigyasu Kalyan | Analysis Lead |

---

## 📌 Executive Summary

India's river ecosystems face increasing pollution due to industrial discharge, sewage overflow, and agricultural runoff. Although the Central Pollution Control Board (CPCB) collects multi-parameter monitoring data, it is rarely converted into actionable intelligence.

This project cleans, analyzes, and visualizes CPCB river water quality data **(2012–2023)** to:

- 🔴 Identify pollution hotspots
- 📈 Track multi-year trends
- 🗺️ Compare state-wise performance
- 🏷️ Classify water quality categories
- 💡 Generate targeted environmental recommendations

The final dashboard transforms **11,718 raw monitoring records** into structured insights supporting:

- Policy prioritization
- State-level intervention
- Hotspot remediation
- Industrial regulation planning

---

## ❓ Problem Statement

How can multi-year CPCB river water quality data be cleaned, analyzed, and visualized to identify pollution hotspots, track trends, rank states by severity, and generate location-specific environmental recommendations?

---

## 📂 Dataset Information

| Field | Details |
|-------|---------|
| **Source Platform** | NITI Aayog – National Data & Analytics Platform (NDAP) |
| **Primary Source** | Central Pollution Control Board (CPCB) |
| **Dataset** | Water Quality of Indian Rivers |
| **Time Period** | 2012–2023 *(2015 missing)* |
| **Rows** | 11,718 (post-cleaning) |

### Parameters Monitored

- Dissolved Oxygen (DO)
- Biochemical Oxygen Demand (BOD)
- pH
- Conductivity
- Nitrate
- Fecal Coliform
- Total Coliform
- Temperature

---

## 🗂️ Project Folder Structure
```
Project Root
│
├── RawDataset/
│   └── dataset.csv
│
├── CleanedDataset/
│   ├── cleaned.csv
│   └── cleaned.md
│
├── Calculations_PivotTables/
│   └── calculations.xlsx
│
├── Dashboard/
│   └── dashboard.pdf
│
├── Presentation/
│   └── presentation.pdf
│
├── Documentation/
│   └── final_report.pdf
│
└── README.md
```

---

## 📊 Analytics Intent

### Key Columns Used

- Year
- State
- Monitoring Location
- BOD (Min/Max)
- DO (Min/Max)
- Nitrate
- pH
- Pollution Flag

---

## 📈 Defined KPIs

| KPI | Purpose |
|-----|---------|
| Avg BOD (`BOD_Avg`) | Primary pollution indicator |
| Avg DO (`DO_Avg`) | River oxygen health |
| Pollution Flag Rate | % of polluted records |
| State Pollution Count | Rank states by count |
| Year-on-Year BOD Change | Trend monitoring |
| Hotspot BOD Ratio | Severity vs national avg |
| Avg Nitrate | Agricultural runoff indicator |
| Avg pH | Chemical stability |

---

## 🔍 Key Insights

- 📉 **National BOD declined 70%** — from 10.16 mg/L (2013) to 3.05 mg/L (2023)
- ⚠️ **31.2%** of monitoring records are Moderate or Polluted
- 🏭 **Maharashtra** leads in pollution count (180 flags)
- 🌾 **Haryana** has the highest average BOD intensity (8.02 mg/L)
- 🚨 **Satluj B/C (Punjab)** hotspot exceeds 175 mg/L BOD — **38.8× the national average**
- 🌿 **COVID lockdown (2020–21)** recorded the cleanest rivers
- 💧 **Nitrate grand average exceeds WHO guideline** (10 mg/L)
- 📍 Pollution is **geographically concentrated**, not uniform

---

## 🧹 Data Cleaning Process

### Issues Found in Raw Dataset

- Missing values
- Inconsistent year format
- Blank station codes
- Extreme outliers
- Redundant columns

### Cleaning Steps

1. Removed rows with blank station codes
2. Renamed Year column
3. Median imputation for missing values
4. Removed Fecal Streptococci columns
5. Created calculated columns:
   - `BOD_Avg`
   - `DO_Avg`
   - `Pollution_Flag`
   - `Pollution_Category`
   - `Nitrate_Avg`
   - `pH_Avg`

---

## 📊 Dashboard Deliverables

The final interactive dashboard includes:

- 📅 Year-wise Pollution Trend
- 🗺️ State-wise Pollution Comparison
- 📊 Pollution Count by State
- 🍩 Pollution Category Distribution
- 🔥 Top Pollution Hotspots
- 📈 State Trend Analysis
- 🌍 Geographic Distribution Map
- 🎛️ 2 Interactive Slicers

---

## 🛠️ Tools & Technologies

- **Google Sheets** — Pivot Tables, Calculated Columns, Charts & Donut Graphs
- **Geo Map** — Geographic visualization
- **GitHub** — Version control & project hosting

---

## 🚀 Business / Policy Impact

This project converts raw CPCB monitoring data into:

- 🎯 Targeted remediation plans
- 📍 Hotspot prioritization
- 📋 State-specific action strategies
- 🏭 Industrial discharge insights
- ⚠️ Environmental risk assessment

> **Key Finding:** Less than 1% of monitoring stations drive a disproportionate share of pollution — making targeted intervention **cost-effective and actionable**.

---

## ⚠️ Limitations

- 2015 data missing
- Some pH data errors
- Annual min/max limits seasonal analysis
- No heavy metals or pharmaceutical residues
- Pollution source attribution not possible

---

## 🔮 Future Scope

- 🧮 Composite River Health Index (CRHI)
- 📊 Time-series forecasting (ARIMA)
- 🔵 Cluster-based pollution typology
- 📡 Real-time IoT sensor integration
- 🗓️ Monthly seasonal pattern analysis

---

## 📩 Contact

For project-related queries:

Adamya Tiwari
adamya.tiwari2024@nst.rishihood.edu.in

---

**Section D – Group 4**<br>
Water Quality of Rivers
