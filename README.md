# Heart Disease Predictor

End-to-end heart disease classification project built as a 7-day roadmap: exploratory data analysis, data cleaning, baseline modeling, advanced models, hyperparameter tuning, interpretability, and final submission packaging.

## Problem Statement

The goal of this project is to predict whether a patient is likely to have heart disease from structured clinical data. The workflow focuses on healthcare-relevant evaluation, especially recall and ROC-AUC, because missed positive cases are more costly than false alarms.

## Dataset

This repository uses multiple heart-disease-related datasets for exploration and model development:

- UCI Heart Disease dataset
- Cardiovascular Disease dataset
- Dataquest competition dataset

The competition test file was used to generate a local `submission.csv` for archive purposes.

## Workflow Summary

The project was developed in the following stages:

1. **Day 1 - EDA**: inspected distributions, missing values, target balance, correlations, and feature-target relationships.
2. **Day 2 - Data Cleaning & Feature Engineering**: handled hidden zeros, removed blood-pressure outliers, converted age units where needed, created age groups, and encoded categoricals.
3. **Day 3 - Baseline Models**: trained Logistic Regression and KNN with stratified validation and ROC-AUC evaluation.
4. **Day 4 - Advanced Models**: trained Random Forest, XGBoost, and SVM, then compared all models side by side.
5. **Day 5 - Model Improvement**: applied GridSearchCV and SMOTE where appropriate.
6. **Day 6 - Interpretation**: added ROC curves, confusion matrices, threshold tuning, and SHAP explainability.
7. **Day 7 - Packaging**: prepared the final notebook, README, and submission artifact for publishing.

## Key Results

| Model | ROC-AUC | Accuracy | Recall | F1 |
|---|---:|---:|---:|---:|
| XGBoost Tuned | 0.9024 | 0.8571 | 0.8889 | 0.8727 |
| Random Forest Tuned | 0.8928 | 0.8231 | 0.8765 | 0.8452 |
| SVM Tuned | 0.8732 | 0.8027 | 0.8395 | 0.8242 |

Threshold tuning on the tuned XGBoost model improved recall to 0.9506 at a threshold of 0.215, which is a better operating point for medical screening.

## Final Files

- `notebooks/heart-disease-detection-and-risk-analysis-final.ipynb` - final polished notebook.
- `data/submission/submission.csv` - archived prediction file generated from the final model.

## Notebook Index

### Final notebook

- `notebooks/heart-disease-detection-and-risk-analysis-final.ipynb` - consolidated notebook with EDA, cleaning, modeling, tuning, interpretation, and submission preparation.

### Working notebooks kept for traceability

- `notebooks/working/heart-disease-detection-and-risk-analysis-eda-1.ipynb` - initial EDA draft.
- `notebooks/working/heart-disease-detection-and-risk-analysis-eda-final.ipynb` - refined EDA version.
- `notebooks/working/heart-disease-detection-and-risk-analysis_data_cleaning.ipynb` - earlier cleaning draft.
- `notebooks/working/heart-disease-detection-and-risk-analysis-data_cleaning_final.ipynb` - cleaned dataset and feature engineering final draft.
- `notebooks/working/heart-disease-detection-and-risk-analysis-baseline-model-2.ipynb` - first baseline modeling iteration.
- `notebooks/working/heart-disease-detection-and-risk-analysis-baseline-model-3.ipynb` - baseline refinement with cross-validation and comparison.
- `notebooks/working/heart-disease-detection-and-risk-analysis-baseline-model-final.ipynb` - final baseline notebook.
- `notebooks/working/heart-disease-detection-and-risk-analysis-advanced-models-1.ipynb` - first advanced-model iteration.
- `notebooks/working/heart-disease-detection-and-risk-analysis-advanced-models-2.ipynb` - advanced-model refinement and comparison.
- `notebooks/working/heart-disease-detection-and-risk-analysis-tuned-models-1.ipynb` - first tuning notebook.
- `notebooks/working/heart-disease-detection-and-risk-analysis-tuned-models-2.ipynb` - tuning notebook with threshold tuning and SHAP.
- `notebooks/working/heart-disease-detection-and-risk-analysis-tuned-models-final.ipynb` - final tuned-model notebook.
- `notebooks/working/heart-disease-detection-and-risk-analysis-shap-1.ipynb` - SHAP exploration draft.
- `notebooks/working/heart-disease-detection-and-risk-analysis-shap-2.ipynb` - SHAP and Day-6 interpretability notebook.

## Submission Note

The Dataquest competition page is closed, so the current `submission.csv` is best treated as an archival artifact rather than an active leaderboard submission.

## How to Reproduce

1. Open `notebooks/heart-disease-detection-and-risk-analysis-final.ipynb`.
2. Run the notebook from top to bottom.
3. Confirm the final cleaned features, tuned model results, and threshold tuning outputs.
4. Generate `data/submission/submission.csv` from the final inference cell.

## Acknowledgements
- Datasets sourced from
    - UCI Heart Disease Detection (https://www.kaggle.com/datasets/johnsmith88/heart-disease-dataset)
    - Cardiovascular Disease dataset (https://www.kaggle.com/datasets/sulianova/cardiovascular-disease-dataset)
    - Heart Disease Prediction with Dataquest (https://www.kaggle.com/competitions/heart-disease-prediction-dataquest)
- Python libraries: pandas, numpy, scikit-learn, xgboost, imbalanced-learn, shap, matplotlib, seaborn.

## License

See `LICENSE` for project licensing details.