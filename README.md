# Air_Quality_Predictor

## Objective: 
Can we accurately predict periods of elevated air quality risk (AQI > 75) using pollutant levels and temporal patterns to enable early public health intervention?

This approach can be especially valuable for protecting sensitive populations such as children, the elderly, and individuals with respiratory conditions. “Predicting AQI” is the main target but we can go further and frame it as a Public health early warning system and identify high-risk locations and high-risk time periods. This model can help communities anticipate periods of poor air quality and take preventive actions such as limiting outdoor exposure, especially for vulnerable populations.

--- 
### Data Source: 
- https://www.epa.gov/outdoor-air-quality-data/download-daily-data
- We’ll use the datasets from here using Pollutant: PM2.5, Geographic Area: California, Monitor Site: All Sites for 2021, 2022, 2023, 2024, and 2025. 

### Target Variable:
- Safe (AQI ≤ 75)
- At Risk (AQI > 75)

### Features to Use:
- PM2.5 concentration (primary pollutant driving AQI)
- Month and Season (to capture temporal and seasonal patterns)
- Location (County) to capture geographic variation in air quality
- Optional: Future work could incorporate additional pollutants and weather data
