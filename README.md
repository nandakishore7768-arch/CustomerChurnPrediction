# Banking Customer Churn Prediction

Predicts whether a bank customer will churn using XGBoost, trained on the Kaggle Banking Customer Churn dataset.

## Results
| Metric | Score |
|--------|-------|
| Accuracy | 0.805 |
| Recall | 0.750 |
| Precision | 0.508 |
| F1 | 0.606 |
| ROC-AUC | 0.784 |

> Model optimized for **Recall** — minimizing missed churners is prioritized over false positives.

## Features
| Feature | Description |
|---------|-------------|
| CreditScore | Customer credit score |
| Geography | Country (France/Spain/Germany) |
| Gender | Male/Female |
| Age | Customer age |
| Tenure | Years with the bank |
| Balance | Account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Has credit card (0/1) |
| IsActiveMember | Active member (0/1) |
| EstimatedSalary | Estimated annual salary |

> `Surname` dropped (no predictive value). `Geography` and `Gender` one-hot encoded → 10 features become 11.

## Project Structure