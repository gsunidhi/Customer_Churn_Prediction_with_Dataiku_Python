# 🌀 Customer Churn Prediction with Dataiku DSS & Python

This project demonstrates an end-to-end customer churn prediction pipeline using [Dataiku DSS](https://www.dataiku.com/) and Python. It includes data cleaning, feature engineering, model training, automated scoring, and dashboarding.

---

## 📂 Dataset
- Source: [Kaggle – Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)
- Sample provided in `data_sample/`

---

## 🧪 Project Steps

1. **Data Ingestion**
   - Load CSV into Dataiku Flow

2. **Data Cleaning (Prepare Recipe)**
   - Handle nulls, unify column formats, and create target column `has_churned`

3. **Feature Engineering (Python Recipe)**
   - Created `spend_per_tenure = MonthlyCharges / (tenure + 1)`

4. **Modeling**
   - Trained binary classification model (Random Forest) using visual ML

5. **Scoring**
   - Applied model to score new data and identify high-risk customers

6. **Automation (Scenario)**
   - Scenario loops through data monthly, scores, and exports high-risk customers

---

## 🔧 Python Recipes

- `feature_engineering.py`: Creates new features
- `export_high_risk.py`: Filters and exports risky customers

---

## 🔁 Automation

- Implemented Dataiku Scenario that:
  - Refreshes data
  - Builds features
  - Scores model
  - Exports customers with churn score > 0.8

---

## 📌 Tools Used
- Dataiku DSS
- Python (pandas)

