# Peakflo Expense Classification

Classify expense transactions into the correct account category (`accountName`) using vendor identity, item descriptions, and transaction amounts.

## Results

- **Best Model:** Logistic Regression (C=5, one-hot vendor encoding)
- **Accuracy:** ~90% on held-out test set (target: 85%)
- **Models compared:** Logistic Regression (90.0%), Random Forest (88.9%), XGBoost (85.6%)
- **Features:** TF-IDF text (3,000) + one-hot vendor (~324) + log amount (1) = 3,325 total

## Dataset

- `accounts-bills.json` — 4,894 expense records with 337 vendors and 103 account categories

## Setup

```bash
pip install -r requirements.txt
```

## Run

Open and run the notebook top-to-bottom:

```bash
jupyter notebook Expense_Classification.ipynb
```

Or via command line:

```bash
jupyter nbconvert --to notebook --execute Expense_Classification.ipynb
```

## Files

| File | Description |
|------|-------------|
| `Expense_Classification.ipynb` | Main notebook — EDA, model training, evaluation |
| `accounts-bills.json` | Dataset (4,894 records) |
| `requirements.txt` | Python dependencies |

## Requirements

- Python 3.8+
- pandas 2.2.0
- scikit-learn 1.4.0
- matplotlib 3.8.2
- seaborn 0.13.2
- xgboost 2.0.3
