# 💳 Credit Card Financial Analytics with Default Risk Prediction (Power BI + ML)

This project analyzes credit card customer behavior, spending patterns, and payment performance using **Power BI** dashboards and **Machine Learning**. The goal is to extract business insights and predict default risk using classification models built in Python.

---

## 📊 Project Objectives

- Build intuitive dashboards to visualize customer trends and financial KPIs.
- Clean and engineer features from transactional and demographic data.
- Train ML models to identify high-risk (likely to default) customer segments.

---

## 📁 Dataset Overview

The project uses four CSV files:

| File Name         | Description                                         |
|-------------------|-----------------------------------------------------|
| `credit_card.csv` | Weekly transaction and credit details per client    |
| `customer.csv`    | Customer demographics and satisfaction scores       |
| `cc_add.csv`      | Credit card metadata                                |
| `cust_add.csv`    | Customer contact and address details                |

---

## 🧹 Data Preparation

- Merged all datasets on the unique customer ID (`Client_Num`).
- Cleaned column names and handled missing values.
- Performed label encoding for categorical variables (e.g., Gender, Card Type).
- Created a `default_flag` (1 = default, 0 = non-default) as the target variable.

---

## 📊 Dashboarding in Power BI

**Power BI dashboards** were created to explore:

- Revenue and interest earnings by card type, age group, and state.
- Spend volume and average utilization by customer segment.
- Delinquency patterns and satisfaction scores.

📸 _Screenshots available in_ `/dashboard_screenshots`.

---

## 🤖 Machine Learning: Default Risk Prediction

### ✅ Models Trained:

- Logistic Regression  
- Decision Tree Classifier  
- Random Forest (with class balancing)  
- XGBoost Classifier (with SMOTE and `scale_pos_weight`)  

### 📊 Evaluation Metrics:

- Accuracy, Precision, Recall, F1-score  
- Confusion Matrix  
- Precision-Recall Curve

> ⚠️ **Challenge:** The dataset is highly imbalanced (~1 default per 100 users).  
> This led to high overall accuracy but poor recall for defaulters.  
> SMOTE oversampling and hyperparameter tuning were used to improve performance.

---

## 📈 Key ML Insights

- Logistic Regression and Decision Tree struggled with class imbalance.
- Random Forest and XGBoost + SMOTE performed better in identifying defaulters.
- Precision-Recall tradeoff visualizations helped optimize decision thresholds.

---

## 🛠️ Tools & Libraries Used

- **Python:** `pandas`, `numpy`, `scikit-learn`, `xgboost`, `imblearn`, `matplotlib`, `seaborn`  
- **Power BI:** KPIs, slicers, drill-downs, stacked visuals, trendlines  

---

## 📌 Key Learnings

- Built ML models for imbalanced classification scenarios.
- Designed dashboards to drive actionable business insights.
- Used SHAP values and feature importance to interpret model decisions.

