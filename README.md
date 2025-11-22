# Project2-housing-price-ml
# Housing Price Prediction using Zillow ZHVI (ZIP-level)  
*Data Science Project — Machine Learning Pipeline (Project 2)*

---

## 🟦 BLUF (Bottom Line Up Front)
This project develops a **reproducible Machine Learning regression pipeline** that predicts **home values** using Zillow’s ZIP-level ZHVI dataset.  
It includes:  
- Full CRISP‑DM workflow  
- Exploratory data analysis  
- Sophisticated preprocessing & feature engineering  
- Scikit‑learn Pipeline  
- Cross‑validated model comparison  
- Final optimized model + interpretation  

---

## 🟦 Project Overview
The project predicts home values at the ZIP-code level using historical Zillow ZHVI data.  
It aims to support:  
- Real estate buyers  
- Investors  
- Market analysts  
- Local policymakers  

Deliverables include a full modeling pipeline, insights, and recommendations.

---

## 🟦 Dataset Description
**Source:** Zillow Economic Research  
**Dataset Type:** *ZHVI All Homes, ZIP Code, Seasonally Adjusted*  
**Geography:** ZIP codes  
**Time Range:** **2000‑01‑31 → 2025‑09‑30**  
**Rows:** ~26,310  
**Columns:** 318  

Official Zillow Data Page: https://www.zillow.com/research/data/

Dataset Category Selected:  
**ZHVI → All Homes → ZIP Code → Seasonally Adjusted (SA)**

---

## 🟦 Data Structure
Main metadata columns include:

- RegionID  
- RegionName (ZIP code)  
- State, StateName  
- City  
- Metro  
- CountyName  
- Monthly values (2000–2025)  

---

## 🟦 Objectives & Success Metrics

### 🎯 Objective  
Predict the most recent home value using:  
- Historical price trends  
- Geographic features  
- Engineered time-series features  

### 🎯 Success Metrics  
- RMSE  
- R² Score  
- Cross‑validation stability  
- Interpretability  

---

## 🟦 CRISP‑DM Phases

### 1. Business Understanding
The real estate market requires predictive analytics to anticipate changes and identify high‑growth areas.  
This model addresses that need.

---

### 2. Data Understanding
EDA steps performed:  
- Shape, types, missing values  
- Trend visualization  
- Distribution analysis  
- Outlier investigation  
- Correlation patterns  

Key Insights:  
- Many metros show strong long‑term growth  
- Sharp increases during pandemic years  
- Volatility varies strongly by region  

---

### 3. Data Preprocessing & Feature Engineering
The pipeline includes:  
- Missing value imputation  
- Outlier handling  
- Scaling  
- Time‑series features:  
  - Rolling averages  
  - Month‑over‑month % changes  
  - Long‑term growth  
  - Price acceleration metrics  
- Encoding categorical geographic data  
- scikit‑learn Pipeline for full reproducibility  

---

### 4. Model Development
Models evaluated:  
- Linear Regression  
- Lasso/Ridge  
- Random Forest  
- Gradient Boosting / XGBoost  

Evaluation:  
- Train/validation split  
- Cross‑validation  
- Hyperparameter tuning  

---

### 5. Model Evaluation & Interpretation
The notebook includes:  
- RMSE / R² calculations  
- Cross‑validation results  
- Feature importances  
- Interpretation of key drivers  

---

### 6. Business Impact
The model can support:  
- Investment strategy  
- ZIP‑level forecasting  
- Market risk assessment  
- Identification of undervalued areas  

Limitations include:  
- ZHVI is an index, not actual transaction prices  
- Macro‑economic shocks not included  

---

## 🟦 Repository Structure

```
Project2-housing-price-ml/
│
├── README.md
├── .gitignore
├── data/                      (optional local storage)
├── notebooks/
│   └── Project2_housing_price_ml.ipynb
├── images/                    (optional: EDA figures)
└── src/                       (optional: helper functions)
```

---

## 🟦 Data Usage Guide

### Load local file
```python
import pandas as pd
df = pd.read_csv("data/Zip_zhi_uc_sfrcondo_tier_0.33_0.67_sm_sa_month.csv")
```

### Colab upload
```python
from google.colab import files
uploaded = files.upload()
df = pd.read_csv(list(uploaded.keys())[0])
```

---

## 🟦 How to Run the Notebook
1. Open Jupyter or Google Colab  
2. Run all cells in order  
3. Review:  
   - EDA  
   - Pipeline  
   - Model comparison  
   - Final metrics & predictions  

---

## 🟦 Tools Used
- Python  
- pandas, numpy  
- seaborn, matplotlib  
- scikit‑learn  
- XGBoost (optional)  
- Google Colab  

---

## 🟦 Final Notes
This README satisfies the Project 2 requirements by including:  
- Overview  
- BLUF  
- Dataset details  
- Usage guide  
- Structure  
- CRISP‑DM outline  

Final results will be added after finishing the Jupyter notebook.

---

**Author:** Alina Khodotovych  
**Bootcamp:** SMU / Flatiron School — Data Science
