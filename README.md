# Customer-Churn-Analysis

## 1. Project Overview  
This repository contains customer churn analysis workflow conducted on Telco data. It includes data acquisition, preprocessing, exploratory data visualization, predictive modeling, and business-focused recommendations. The analysis uses the Telco Customer Churn dataset and demonstrates advanced applied analytics with reproducibility and translation to real business decisions.


## 2. Objective  
- Predict which customers are likely to leave  
- Understand key drivers of churn in telecom subscriptions  
- Quantify impact of churn reduction on revenue and retention effort  
- Provide actionable retention strategy based on model insights  


## 3. Data Source  
- `Telco customer churn data.csv`  
- Columns include demographics, service details, account info, and churn target (`Yes`/`No`).  
- Common domain features: `tenure`, `MonthlyCharges`, `TotalCharges`, `Contract`, `PaymentMethod`, `InternetService`, etc.



## 4. Tools & Libraries  
- Python 3.11+  
- pandas, numpy  
- matplotlib, seaborn  
- scikit-learn (train_test_split, LabelEncoder, StandardScaler, LogisticRegression, RandomForestClassifier, metrics)



## 5. Notebook Layout (customer_churn_analysis.ipynb)

1. **Step 1: Import libraries**  
2. **Step 2: Load data**  
   - Path: `/Users/enika/Desktop/Customer churn/Telco customer churn data.csv`  
   - Initial quality check: shape, head, column list  
3. **Step 3: Data exploration**  
   - info(), null counts, churn distribution  
4. **Step 4: Clean data**  
   - Drop customerID  
   - `TotalCharges` numeric conversion + missing-imputation  
   - Encode churn target: `Yes=1`, `No=0`  
5. **Step 5: EDA**  
   - 6-panel chart: churn distribution, contract churn rates, tenure, monthly charges, correlation, summary  
6. **Step 6: Modeling prep**  
   - Label encoding all object columns  
   - x/y split, scaling, train/test  
7. **Step 7: Model training**  
   - Logistic Regression  
   - Random Forest  
8. **Step 8: Model eval**  
   - Confusion matrix, ROC curves, feature importance  
9. **Step 9: Business recommendations**  
   - retention actions and forecasts (5% churn reduction impact)



## 6. Key Findings (example results)  
- Churn rate ~ `XX%` (computed by code)  
- Month-to-month contracts are highest risk  
- `tenure`, `MonthlyCharges`, `Contract` top predictors  
- Random Forest likely chosen as best model (AUC comparison)



## 7. Interpretation + Action Plan  
- Execute retention campaigns for customers with high churn probability  
- Prioritize early-tenure clients and high monthly charges  
- Offer contract migration incentives (month-to-month → annual)  
- Track feature shifts by cohort and update model quarterly  



## 8. Output files  
- `churn_eda.png`  
- `churn_model_results.png`  
- `customer_churn_analysis.ipynb`  
