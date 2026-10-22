# Airline Passenger Satisfaction Prediction

## Project Overview
This project applies statistical learning methods to predict airline passenger satisfaction using machine learning classification models. The goal is to compare model performance, evaluate generalization ability, and identify the key factors associated with passenger satisfaction.

## Dataset
- **Observations:** Approximately 130,000 passengers
- **Target variable:** Passenger satisfaction
- **Task:** Binary classification

## Methods
Three classification models were implemented and compared:

- **Logistic Regression** — baseline model, tuned using `GridSearchCV` with different regularization strengths (`C`).
- **Random Forest** — tuned using `GridSearchCV` to optimize parameters such as `n_estimators`, `max_depth`, `max_features`, and `min_samples_leaf`.
- **Gradient Boosted Trees (GBT)** — tuned using `RandomizedSearchCV` to explore `n_estimators`, `learning_rate`, `max_depth`, and `subsample`.

Model evaluation included ROC-AUC, confusion matrices, and feature importance analysis.

## Results

| Model | Train AUC | Test AUC |
|---|---:|---:|
| Logistic Regression | 0.8433 | 0.8452 |
| Random Forest | 0.8835 | 0.8718 |
| Gradient Boosted Trees | 0.8756 | **0.8719** |

Gradient Boosted Trees was selected as the final model because it achieved the highest test ROC-AUC and had a small train-test gap, indicating good generalization performance.

Feature importance analysis highlighted travel type, customer loyalty status, and travel class as important predictors of passenger satisfaction.

## Tools & Libraries
- Python
- Pandas and NumPy
- Scikit-learn
- Matplotlib and Seaborn
- Jupyter Notebook

## Key Learning Outcomes
- Hyperparameter tuning and cross-validation
- Model evaluation using ROC-AUC and confusion matrices
- Overfitting and generalization analysis
- Feature importance interpretation

## Project Structure
```text
├── notebooks/       # Data analysis and model development
├── outputs/         # Evaluation results and visualizations
└── README.md        # Project documentation
```

##Authors
JING TAN 
Aleksandra Osińska
Laura Tabaczyńska
