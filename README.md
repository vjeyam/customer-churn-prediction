# Customer Churn Prediction

In this notebook, we explore the problem of customer churn prediction using the `Telco Customer Churn` dataset from [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data). The dataset contains information about customers of a telecommunications company, including their demographics, service usage, and churn status.

The goal is to reduce churn by building a machine learning model that estimates each customer's probability of churning. I built and evaluated several models, including Logistic Regression, Random Forest, and Gradient Boosting. Based on performance metrics (accuracy, precision, recall, and F1-score), the Gradient Boosting model outperformed the others, making it the recommended approach for churn prediction.
![Model Performance Metrics](assets/model-comparison.png)
*Figure 1: Comparison of model performance across ROC-AUC and PR-AUC metrics*

## 1. Dataset Overview

The dataset consists of approximately 7,000 customers and includes the following types of information:

- Customer demographics (e.g., gender, senior citizen status)
- Account details (e.g., tenure, contract type, payment method)
- Subscribed services (e.g., internet service, streaming, tech support)
- Billing information (monthly and total charges)

The target variable is customer churn, a binary indicator showing whether a customer left the company.

## 2. Approach

The project follows a standard end-to-end data science workflow:

1. **Exploratory Data Analysis (EDA)**
   - Examined churn distribution and class imbalance
   - Analyzed churn patterns by tenure, contract type, pricing, and services

2. **Feature Engineering & Preprocessing**
   - Encoded categorical variables
   - Scaled numerical features
   - Used pipelines to prevent data leakage

3. **Modeling**
   - Logistic Regression (baseline & interpretability)
   - Random Forest
   - Gradient Boosting

4. **Evaluation & Comparison**
   - ROC-AUC
   - Precision-Recall AUC
   - Confusion matrices and business-oriented interpretation

## 3. Key Insights

Several factors are strongly associated with customer churn:

- Month-to-month contracts have significantly higher churn rates
- Newer customers are more likely to churn than long-tenured customers
- Higher monthly charges correlate with increased churn
- Lack of support services (e.g., tech support, online security) increases churn risk

These insights suggest that both pricing pressure and perceived service value play important roles in customer retention.

## 4. Business Recommendations

Based on the model results and insights:

- Prioritize high-risk customers for retention campaigns
- Encourage long-term contracts to reduce churn
- Offer discounts or service bundles to customers with high monthly charges
- Promote support and security services to improve perceived value

In this context, recall is prioritized over precision, as missing a churner is more costly than targeting a customer who would have stayed.
