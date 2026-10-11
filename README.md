# Banking Customer Churn Prediction

Predicts whether a bank customer will churn using XGBoost, trained on the Kaggle Banking Customer Churn dataset.

## Results

```
| Metric    | Score |

| Accuracy  | 0.805 |
| Recall    | 0.750 |
| Precision | 0.508 |
| F1        | 0.606 |
| ROC-AUC   | 0.784 |

```

model optimized for Recall while keeping accuracy at a considerable amount

## Features

```
| Feature           | Description |

| CreditScore       | Customer credit score |
| Geography         | Country (France/Spain/Germany) |
| Gender            | Male/Female |
| Age               | Customer age |
| Tenure            | Years with the bank |
| Balance           | Account balance |
| NumOfProducts     | Number of bank products used |
| HasCrCard         | Has credit card (0/1) |
| IsActiveMember    | Active member (0/1) |
| EstimatedSalary   | Estimated annual salary |

```

11 features after changes

## Project Structure

```
├── datasets/
│   ├── training_dataset.csv
│   ├── validation_dataset.csv
│   └── testing_dataset.csv
├── notebooks/
│   ├── EDA.ipynb
│   ├── splitting_preprocessing.ipynb
│   ├── ANN.ipynb
│   └── model_selection.ipynb
├── model.pkl
└── api/              # FastAPI (coming soon)
```

## Model Details
- **Algorithm:** XGBoost (`max_depth=7`, `learning_rate=0.01`, `n_estimators=1000`)
- **Threshold:** 0.2 (tuned for recall)
- **Preprocessing:** StandardScaler