# Climate Resilience Analysis: 25-Year Agricultural Trends in Baranya

### **Executive Summary**
As an international student living in Hungary, I analyzed 25 years of meteorological data from the **NOAA Global Surface Summary of the Day** to understand how climate change is affecting the agricultural heart of the country. Using **SQL** for data engineering and **Power BI** for storytelling, this project identifies critical warming trends and peak temperature risks that threaten the resilience of regional vineyards and crops.

---

## The Tech Stack
* **SQL (Google BigQuery):** Data extraction from wildcard tables, cleaning, and unit standardization.
* **Power BI:** Data modeling, time-series visualization, and KPI dashboarding.
* **Data Source:** NOAA Global Database (2000 - 2025).

---

## Dashboard Preview
> ![Dashboard](grafica%20de%20baranya.png) 
> *Figure 1: Visualizing 25 years of temperature evolution and rainfall averages in Baranya.*

---

## The Business Problem
Farmers and winemakers in the Baranya region (specifically in the Villány area) have noticed increased volatility in crop yields. This project aims to answer:
1.  **Is there a statistically significant warming trend over the last 25 years?**
2.  **What are the historical temperature peaks that trigger irrigation alerts?**
3.  **How has the annual rainfall baseline shifted?**

---

## Technical Process

### 1. Data Engineering (SQL)
The raw data was distributed across 25 separate tables. I used **SQL** to consolidate over 9,000 daily records and handled sensor errors using `NULLIF` and `COALESCE`. 
* **Standardization:** Temperatures were converted from tenths of degrees Celsius to standard Celsius units.
* **Wildcard Queries:** Efficiently queried multiple years of data using `_TABLE_SUFFIX`.

### 2. Data Visualization (Power BI)
* **Trend Analysis:** A dashed trend line was implemented to show the shift from an 11.5°C average to the recent 13.8°C peak.
* **KPI Cards:** Created custom measures to highlight the **Historical Temperature Peak (31.89°C)** and **Average Annual Rainfall (1.76mm)**.

---

## Key Insights & Results
* **Warming Acceleration:** The data shows a clear upward trajectory starting in 2017. The average annual temperature has increased by approximately **2.3°C** from the 2005 baseline.
* **Critical Peaks:** The peak temperature of **31.89°C** serves as a vital threshold for heat-stress prevention in local agriculture.
* **Dry Spells:** The consistency of low rainfall (1.76mm avg) combined with rising heat indicates a high risk of soil moisture depletion.

---

## Business Recommendations
1.  **Adaptive Irrigation:** Regional planners should adjust water allocation schedules based on the new 13.5°C baseline established in the last 3 years.
2.  **Heat-Resistant Crops:** Vineyard owners should consider diversifying with grape varieties that thrive in the warmer "New Normal" identified in this study.
3.  **Predictive Alert System:** Use the historical peak data to set automated alerts when 10-day forecasts exceed the 90th percentile of this dataset.

---
## About the Author
**Maria Castillo** 
