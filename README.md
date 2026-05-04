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

---

## Data Access

Due to file size limitations, datasets are stored in Google Drive:

👉 **[INSERT YOUR GOOGLE DRIVE LINK HERE]**

---

## How to Run This Project

1. Open the dataset link above  
2. Click **“Add shortcut to Drive”**  
3. Ensure the folder is saved directly in **My Drive**  
4. Open the notebook in **Google Colab**  
5. Run the following to mount Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

## Models Used

Three classification models were implemented:

- **Logistic Regression** — baseline interpretable model  
- **Random Forest** — captures nonlinear relationships and feature interactions  
- **XGBoost** — boosting method for improved performance  

---

## Model Evaluation

Due to class imbalance (~2% unsafe AQI days), accuracy alone is not sufficient.

We prioritized:

- **AUC (Area Under ROC Curve)** — overall classification performance  
- **Recall (Class 1)** — ability to detect unsafe AQI days  
- **Precision (Class 1)** — minimizing false alarms  

---

## Key Findings

- **PM2.5 is the dominant predictor** of AQI levels  
- Models achieved near-perfect performance when PM2.5 was included (AUC ≈ 0.999+)  
- Removing PM2.5 significantly reduced model performance  
- Other variables (ozone, population, weather) provide additional but weaker signal  

---

## Final Model

The **Tuned Random Forest** was selected as the final model due to its balance between precision and recall.

---

## Limitations

- Heavy reliance on PM2.5 limits generalizability  
- Severe class imbalance (~2% unsafe days)  
- Limited external features (e.g., traffic, industrial activity)  

---

## Future Improvements

- Incorporate additional environmental and policy data  
- Apply time-series modeling techniques  
- Enhance feature engineering (spatial + temporal patterns)  

---

## Repository Structure


---

## Requirements

Install dependencies using:

```bash
pip install -r requirements.txt
```

---

## Conclusion

This project demonstrates that unsafe AQI levels can be predicted with high accuracy, with **PM2.5 serving as the most critical feature**. The model highlights the importance of environmental monitoring in supporting public health decision-making.
