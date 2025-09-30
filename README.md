# gestational-diabetes-prediction-ml
Predicting gestational diabetes from the Pima dataset — Python (scikit-learn); reproducible notebook, metrics, and report.
# Gestational Diabetes Prediction — Python (scikit-learn)

**Purpose.** Build a reproducible classification baseline for early GDM risk using the (public) Pima Diabetes data; show data cleaning/validation, model comparison, and clear metrics.

## Data
- Source: Kaggle Pima Indians Diabetes (public).  
- This repo includes only a tiny **/data/sample/** snippet; instructions to obtain the full dataset are below.

## Approach (quick)
- **Data cleaning/validation:** remove duplicates; impute invalid zeros (mean/median by distribution); basic sanity checks.
- **EDA & feature selection:** class balance, histograms, correlations; Pearson-based feature screening.
- **Modeling:** train/test split (80/20); compare **Logistic Regression**, **Random Forest**, **SVM**; **GridSearchCV** for tuning.
- **Evaluation:** accuracy, precision, recall, F1; confusion matrices.

## Results (example — replace with yours)
- **Best model:** SVM — **Acc ~0.78 • P 0.64 • R 0.63 • F1 0.64** on hold-out.
- Confusion matrix: ![SVM](reports/figures/confusion_matrix_svm.png)

## How to run
```bash
# create env
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# open the notebook
jupyter notebook notebooks/code.ipynb
