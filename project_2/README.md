# Student Performance Factors — Exam Score Prediction

Exploratory data analysis and regression modeling to identify the key factors
driving student exam performance.

## Dataset

`StudentPerformanceFactors.csv` — 6,607 records, 20 features covering study
habits, attendance, parental involvement, access to resources, sleep,
motivation, and more, with `Exam_Score` as the target variable.

> Place the CSV file in the project root before running the notebook.

## Project Workflow

1. **Data Cleaning** — handling missing values (numeric imputation via
   median, categorical imputation via mode), type coercion.
2. **Exploratory Data Analysis** — distribution plots, correlation analysis.
3. **Feature Engineering** — encoding categorical variables, scaling.
4. **Modeling** — comparison of:
   - Ridge Regression
   - Random Forest Regressor
   - XGBoost Regressor
5. **Evaluation** — RMSE and R² score comparison across models.
6. **Feature Importance** — coefficient analysis from the best-performing
   model to identify top drivers of exam scores.

## Key Findings

Top factors positively/negatively influencing exam scores:

| Feature | Impact |
|---|---|
| Attendance | Strong positive |
| Hours Studied | Strong positive |
| Access to Resources (Low) | Negative |
| Parental Involvement (Low) | Negative |
| Previous Scores | Positive |

## Setup

```bash
pip install -r requirements.txt
jupyter notebook main.ipynb
```

## Tech Stack

- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn
- xgboost
