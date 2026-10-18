# Machine Learning Notes

> **Archived.** This is a 2018 course/learning project and is no longer maintained.

Personal notes and code templates from the Udemy course "Machine Learning A-Z". Each folder contains a Python template (and, where available, an R version) for one step of a typical supervised-learning workflow: data preprocessing and random forest classification on small example datasets.

## Tech stack

- Python 3 with NumPy, pandas, matplotlib, scikit-learn
- R (for the `.R` versions of the classification scripts)

## Repository structure

- `Data_Preprocessing/` - missing-data handling, encoding, train/test split and feature scaling template (`data_preprocessing_template.py`) with its `Data.csv` example
- `Random_Forest_Classification/` - Python and R random forest classification scripts and templates, using `Social_Network_Ads.csv`

## How to run

From the folder that contains the script (the scripts read their CSV files with relative paths):

```
pip install -r requirements.txt
cd Data_Preprocessing
python data_preprocessing_template.py

cd ../Random_Forest_Classification
python random_forest_classification.py
```

Note: some templates use APIs that were removed in newer scikit-learn releases (`sklearn.preprocessing.Imputer` and `sklearn.cross_validation`). They were written for scikit-learn versions before 0.20 and will fail on current versions unless those imports are changed to `sklearn.impute.SimpleImputer` and `sklearn.model_selection`.
