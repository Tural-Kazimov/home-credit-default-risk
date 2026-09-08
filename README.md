# Home Credit Default Risk

A credit risk modeling project based on the Home Credit Default Risk dataset. The goal is to predict repayment difficulties and study the full model development and validation process.

## Project Progress

The project currently includes exploratory data analysis, preprocessing, and a baseline Logistic Regression model. WOE/IV analysis and further model development are in progress.

| Notebook | Description |
|---|---|
| `01_data_analysis_and_preprocessing.ipynb` | EDA, data quality checks, and initial preprocessing |
| `02_model_development.ipynb` | Train-validation split, imputation, encoding, scaling, and saved datasets |
| `03_model_training.ipynb` | Baseline modeling, performance evaluation, threshold analysis, and further development |

## Baseline Results

The baseline Logistic Regression uses application data only.

| Metric | Train | Validation |
|---|---:|---:|
| ROC-AUC | 0.7512 | 0.7506 |
| Gini | 0.5023 | 0.5011 |
| Average Precision | 0.2290 | 0.2356 |

The model shows useful ranking ability. Threshold analysis demonstrates the trade-off between detecting clients with repayment difficulties and generating false positives. No final operational threshold has been selected.

## Data and Reproducibility

The original data is available from the [Home Credit Kaggle competition](https://www.kaggle.com/competitions/home-credit-default-risk/data).

The `model_data/` directory contains saved train and validation datasets, allowing users to inspect the prepared data or continue directly with model training. Large raw and preprocessed CSV files are excluded from GitHub.

To reproduce the full workflow, download the dataset, place the application data in `data/`, and run the notebooks in numerical order. The project uses Python, pandas, NumPy, scikit-learn, Matplotlib, Seaborn, joblib, and optbinning.

## Next Steps

WOE/IV analysis, alternative modeling approaches, feature engineering, and deeper model validation, including calibration and stability analysis.

This project is for learning and portfolio purposes and is not a production credit decision system.

## Status

The project is currently under development. Model development and evaluation will be added in later stages.