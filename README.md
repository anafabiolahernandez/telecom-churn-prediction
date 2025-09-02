# Customer Retention Plan for Telecommunications (Sep 2025)

## Overview
This project focuses on predicting customer churn in a telecommunications company using **Random Forest**, **Decision Tree**, and **Logistic Regression** models. The goal is to identify customers at risk of leaving the service and propose actionable retention strategies.

The analysis includes:

- Exploratory Data Analysis (EDA)
- Feature engineering, including creation of synthetic variables
- Handling class imbalance with **SMOTE-TOMEK**
- Model evaluation and comparison
- Business implications and actionable recommendations

## Dataset
The dataset contains information on **3,150 clients**, including both active customers and those who have churned. Key variables include:

- Call Failure
- Complaints
- Subscription Length
- Charge Amount
- Seconds of Use
- Frequency of Use
- Frequency of SMS
- Distinct Called Numbers
- Age Group
- Tariff Plan
- Status
- Age
- Customer Value

## Methodology

1. **Data Cleaning & EDA**
   - Removed duplicates and null values
   - Analyzed distributions with **boxplots**
   - Explored correlations with a **heatmap** and identified key variables

2. **Feature Engineering**
   - Created synthetic variables:
     - `FrequencyPerMonth` (to reduce collinearity)
     - `ChargePerMonth`
   - Checked relevance using a **Decision Tree**

3. **Handling Imbalanced Classes**
   - Applied **SMOTE-TOMEK** to balance churned vs. retained customers

4. **Modeling**
   - **Random Forest**: high performance without scaling, reduces overfitting risk
   - **Decision Tree**: interpretable, captures non-linear patterns
   - **Logistic Regression**: scaled numerical variables for better performance

5. **Evaluation**
   - Metrics: Accuracy, Recall, F1-Score, ROC-AUC
   - Random Forest outperformed all other models:
     - Accuracy: 0.97
     - Recall (churners): 0.98
     - F1-Score (churners): 0.97
     - ROC-AUC: 0.987

## Business Implications
- Customers predicted to churn with >50% probability should be prioritized for retention actions:
  - Direct communication to resolve complaints
  - Offer packages with extended coverage or unlimited calls
  - Targeted discounts and infrastructure improvements
- Benefits include:
  - Reduced churn
  - Increased new customer acquisition in high-coverage areas
  - Diversification of the customer base
  - Personalized service for at-risk customers
  - Improved reputation and customer satisfaction

## Technologies & Libraries
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- scikit-learn (RandomForestClassifier, DecisionTreeClassifier, LogisticRegression)
- imblearn.combine (SMOTETomek)
- ydata-profiling (for automated EDA)

## Author
**Ana Hernández**  
Aspiring Data Analyst
