# Air Quality Predictor

### Predicting Unsafe Air Quality (AQI > 100) Using Environmental, Weather, and Demographic Data

**Authors:**  
Bhavna Sreekumar  
Sarkis Shil-Gevorkyan  
Christopher Strouse  

---

## Project Objective

The goal of this project is to predict whether a given day will experience **unsafe air quality (AQI > 100)** using environmental, weather, and demographic features.

This problem is important because poor air quality has significant public health impacts, particularly in densely populated regions. By accurately predicting unsafe AQI days, this model can support early warnings and preventative action.

---

## Predictive Questions

- **Primary Question:**  
  Can we accurately predict whether AQI will be unsafe using historical environmental and demographic data?

- **Secondary Question:**  
  Which features have the strongest influence on unsafe AQI levels?

---

## Dataset

The dataset combines multiple sources:

- **Environmental Data:** PM2.5, Ozone  
- **Weather Data:** Temperature, Wind, Precipitation  
- **Temporal Features:** Season, Weekend  
- **Demographic Data:** Population  

> Note: Due to file size, datasets are stored externally (see Data Access section below).

---

## Data Access

Datasets are hosted in Github under "Datasets" 

### To Run the Notebook:

1. Open the dataset link  
2. Click **“Add shortcut to Drive”**  
3. Mount Drive in Colab:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
