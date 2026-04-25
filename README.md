Climate Resilience Analysis: 25-Year Agricultural Trends in Baranya
Earth Science & Data Analytics for Precision Viticulture
1. Executive Summary
As an Earth Science student based in Hungary, I analyzed 25 years of meteorological data from the NOAA to understand the climate shift in the Baranya region. This project identifies warming trends and peak temperature risks that impact regional vineyards, specifically in the Villány wine district.

2. The Tech Stack
SQL: Google BigQuery

Data Cleaning: Microsoft Excel

Visualization: Power BI

Data Source: NOAA Global Database (2000-2025)

3. Technical Process: Data Engineering (SQL)
I implemented a SQL pipeline to consolidate data across 25 years, handling unit conversion from imperial to metric and managing sensor null values for precipitation.
 ```sql
SELECT
  CONCAT('20', _TABLE_SUFFIX) AS year,
  ROUND((temp-32)*5/9,2) AS avg_temp_c,
  ROUND(NULLIF(prcp,99.99)*25.4,2) AS rain_mm,
  ROUND((max-32)*5/9,2) AS max_temp_c,
  ROUND((min-32)*5/9,2) AS min_temp_c
FROM
  `bigquery-public-data.noaa_gsod.gsod20*`
WHERE
  stn = '129420'

4. Dashboard Preview
Figure 1: 25-year evolution of temperature and rainfall in Baranya.

5. Key Insights & Results
Warming Acceleration: The average annual temperature has increased from an 11.5°C baseline to a recent 13.8°C peak.

Critical Thresholds: Historical peaks near 32°C serve as vital indicators for heat-stress prevention in local crops.

Hydrological Shift: The consistency of low rainfall averages (1.76mm) combined with rising heat indicates a high risk of soil moisture depletion.

6. Business Recommendations
Adaptive Irrigation: Adjust water allocation schedules based on the new 13.5°C baseline.

Heat-Resistant Crops: Diversify with grape varieties that thrive in the identified "New Normal."

Predictive Alert System: Use historical peak data to set automated alerts for extreme heat events.

Author
María Castillo
  AND _TABLE_SUFFIX BETWEEN '00' AND '25'
ORDER BY 
  year ASC;
