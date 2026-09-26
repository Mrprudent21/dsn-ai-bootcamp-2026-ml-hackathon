# DSN AI Bootcamp 2026 ML Qualification Hackathon

## DSN Mart Product-Store Sales Prediction

This repository contains my project work for the DSN AI Bootcamp 2026 Machine Learning Qualification Hackathon.

### Objective

The task was to predict `total_sales` for product-store observations in the competition test set.

### Modelling approach

The project followed a simple, reproducible modelling workflow:

1. Loaded and audited the training and test data.
2. Examined the target distribution, store-level sales patterns, product price, and missing values.
3. Used 5-fold cross-validation on the training data for model comparison.
4. Compared a mean-sales baseline, Ridge regression, and two CatBoost regression configurations.
5. Selected the model with the lowest mean cross-validation RMSE.
6. Retrained the selected model on the full training data.
7. Generated and checked the Kaggle submission file.

### Results

| Model | Mean CV RMSE |
|---|---:|
| Mean baseline | 1697.7241 |
| Ridge regression | 1137.6723 |
| CatBoost base | 1084.9781 |
| CatBoost tuned | 1078.3807 |

The tuned CatBoost configuration was selected because it produced the lowest mean RMSE among the models evaluated under the same 5-fold validation procedure.

The resulting submission achieved a **Kaggle public RMSE of 1079.58071**.

The cross-validation result and Kaggle public score are reported separately because they come from different evaluation settings.

### Repository contents

- `DSN_2026_ML_Qualification_Hackathon_Submission_Notebook.ipynb` - executed project notebook.
- `requirements.txt` - Python packages used for the project.
- `outputs/cv_model_comparison.csv` - model comparison results.
- `outputs/experiment_log.csv` - experiment record.

The competition data files are not included in this repository.
