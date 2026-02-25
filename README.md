# Bank Customer Churn – Driver Analysis Using Logistic Regression


## Project Overview

This project analyzes customer churn in a anonymous multinational banking dataset to identify the key features that drive customer exit behavior. Data source is obtained from [Kaggle](https://www.kaggle.com/datasets/radheshyamkollipara/bank-customer-churn).

The focus of this study is interpretability and business insight. A logistic regression (logit) model was used to:

- Identify statistically significant drivers

- Quantify impact using odds ratios

- Translate model results into business recommendations


## Business Objective

The goal is to understand what factors increase the likelihood of customer churn and to connect those findings to actionable retention strategies.

This is a driver analysis project, not a deployment-ready production system.


## Methodology

### 1. Data Preprocessing

- Train-test split performed before modeling

- Categorical encoding

Dataset contains ~20.4% churned customers

### 2. Logistic Regression Model

- A logistic regression model was fitted to estimate churn probability.

- Model outputs were interpreted using odds ratios to quantify risk impact.

- Main drivers identified: Credit score, age, balance, geographical location, gender, activeness.
### 3. Threshold Optimization

- ROC-AUC analysis

- Precision-Recall curve

Final performance at selected threshold:

- Recall: 70%

- Precision: 38%

- F1 Score: 50%

The threshold balances churn detection with intervention cost efficiency.

### 4. Expected Profit Framework

To align model performance with business value, an expected profit equation was introduced:

$$ \textrm{Expected Profit} = ( \textrm{TP} × \textrm{Customer Lifetime Value}) − ( \textrm{FP} × \textrm{Retention Cost}) $$

Using the confusion matrix,assume customer lifetime value is \$1000 and retention cost offer is \$100. We obtained a profit of \$60,600


## Future Improvements

- Compare with tree-based models (e.g., XGBoost)

- Perform feature stability analysis

- Conduct uplift modeling for campaign optimization

- Extend to out-of-time validation








