# 📶 Cellular Network Data Analysis  

[![Made with Excel](https://img.shields.io/badge/Made%20with-Excel-217346?logo=microsoft-excel&logoColor=white)]()
[![Visualized in Power BI](https://img.shields.io/badge/Visualized%20in-Power%20BI-F2C811?logo=power-bi&logoColor=black)]()
[![Built for Android](https://img.shields.io/badge/Built%20for-Android-3DDC84?logo=android&logoColor=white)]()
[![Project: Binghamton University](https://img.shields.io/badge/Project-Binghamton%20University-005B33)]()
[![License: Academic](https://img.shields.io/badge/License-Academic-blue)]()

> **CS 527 — Mobile System Security**  
> **School of Computing, Binghamton University**  
> **Authors:** Suraj Kumar & Sumit Nautiyal  
> **Instructor:** Dr. Guanhua Yan  
> 📅 *May 2025*

---

## 🧭 Project Overview

This project investigates **real-world cellular network behavior** by analyzing data collected using the **Network Survey App** integrated with the **SpeedView Speedometer**.  
Our objective was to identify **signal-strength patterns, tower switching behavior, network stability, and provider performance** across various mobility states — *home, campus, and transit* — in and around Binghamton, NY.

Data preprocessing and classification were performed in **Microsoft Excel**, and interactive dashboards were created in **Power BI** to visualize communication-network performance.

---

## ⚙️ Tech Stack

| Category | Tools / Technologies |
|-----------|----------------------|
| **Mobile Data Collection** | Network Survey (Android), SpeedView (Speedometer) |
| **Data Processing** | Microsoft Excel |
| **Visualization & Analytics** | Power BI |
| **Programming Updates** | `build.gradle`, `fragment_network_details.xml` |
| **Test Device** | Samsung S23 FE |
| **Platform** | Android 14 |

---

## 🧪 Methodology

### 🔹 Application Enhancement
- Integrated **Speedometer functionality** within the Network Survey App.  
- Modified **`build.gradle`** and **`fragment_network_details.xml`** for real-time speed and signal visualization.

### 🔹 Data Collection
- Collected live cellular-network data during:
  - 🏠 **Home** (stationary)  
  - 🎓 **University** (indoor/outdoor campus)  
  - 🚗 **Transit** (walking, bus rides, driving)
- Captured attributes:  
  `deviceTime`, `latitude`, `longitude`, `eci`, `earfcn`, `provider`, `speed`, `networkRegistrationInfo`, `rsrp`, `rsrq`.

### 🔹 Data Cleaning & Classification
- Imported CSV files into Excel for preprocessing.  
- Tagged records by **location context** (Home, University, Transit).  
- Detected **tower handovers** via `eci` changes.  
- Calculated metrics for **signal strength**, **network stability**, and **provider performance**.

---

## 📈 Key Results

| Metric | Observation | Insight |
|--------|--------------|----------|
| **Avg Signal Strength** | −62.44 dBm | Stable overall coverage |
| **Min / Max Signal** | −109 / −51 dBm | Occasional weak spots |
| **Strongest Signal** | Home (−58.7 dBm) | Best indoor performance |
| **Weakest Signal** | Transit (−64.7 dBm) | Instability during motion |
| **Unique Towers** | 65 | Broad tower coverage |
| **Tower Switches** | 49 533 | High handover activity |
| **Network Type** | LTE dominant | 5 G available in limited zones |
| **Provider Comparison** | T-Mobile failure ≈ 33 % vs AT&T ≈ 27 % | AT&T slightly more stable |

---

## 🖼️ Visualization Highlights

Interactive **Power BI** dashboards visualize:
- **📊 Signal-Strength Heatmaps** by location  
- **🌐 Network Stability** (5 G vs LTE vs GSM)  
- **🚀 Mobility Impact** comparison (stationary vs transit)  
- **📡 Provider Performance** analysis  

*(Exported dashboards and images are available in the `/visuals` folder.)*

---

## 🧠 Key Findings

- **LTE dominates** network connectivity; **5 G** remains limited.  
- **Signal stability** highest at home, moderate on campus, lowest in transit.  
- **Frequent tower switches** during motion suggest handover inefficiencies.  
- **Provider performance varies by region** — no single provider is consistently dominant.  
- Findings can help optimize future handover logic and coverage planning.

---

## 🧩 Repository Structure

📁 Cellular-Network-Analysis
│
├── 📄 README.md # Project documentation (this file)
├── 📂 data/ # Raw CSV data from Network Survey App
├── 📂 visuals/ # Power BI dashboards / exports
├── 📂 app/ # Android app modified files
├── 📄 analysis.xlsx # Excel preprocessing & calculations
└── 📄 P3_CELLULAR_DATA_ANALYSIS_SUMIT.pdf # Full project report