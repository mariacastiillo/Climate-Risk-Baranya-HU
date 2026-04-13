-- 25-Year Climate Trend Analysis (2000-2025)
-- Author: María Castillo

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
  AND _TABLE_SUFFIX BETWEEN '00' AND '25'
ORDER BY 
  year ASC, date ASC;
