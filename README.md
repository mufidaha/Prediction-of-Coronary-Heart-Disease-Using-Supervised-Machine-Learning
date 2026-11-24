# Prediction of Coronary Heart Disease Using Supervised Machine Learning

**[📊 View the interactive dashboard](https://mufidaha.github.io/Prediction-of-Coronary-Heart-Disease-Using-Supervised-Machine-Learning/)**

## The question
Which risk factors are linked to coronary heart disease (CHD), and which model best identifies patients who have it?

## Key findings
- **Age, lifetime tobacco use and LDL cholesterol** are the strongest drivers in the random forest model.
- CHD rate climbs from **7% (ages 15–29) to 58% (ages 50–59)**; patients with a family history have CHD at about twice the rate (50% vs 24%).
- **Accuracy can mislead on imbalanced health data:** the SVM had the highest accuracy (71%) but caught only **7% of CHD cases**. Logistic regression had the best AUC (0.745) with 50% recall.

## Data
South African Heart Disease dataset (462 patients, 9 risk factors, 35% with CHD; public, distributed with *The Elements of Statistical Learning*). No missing values.

## Method
1. Load and profile the data (shape, types, missing values, distributions, correlation heatmap)
2. Encode family history, split 70/30 (`random_state=7`)
3. Train decision tree, SVM, random forest, logistic regression, k-nearest neighbors and XGBoost
4. Compare accuracy, AUC, precision and recall; review feature importance

| Model | AUC | Accuracy | Recall |
|---|---|---|---|
| Logistic Regression | 0.745 | 69.1% | 50.0% |
| Support Vector Machine | 0.738 | 71.2% | 7.1% |
| Random Forest | 0.727 | 69.1% | 52.4% |
| XGBoost | 0.713 | 71.2% | 61.9% |

## Files
- `MA_CHDMLPRED-2.ipynb` — original notebook (Google Colab)
- `index.html` — dashboard (served by GitHub Pages)

## Tools
Python · pandas · scikit-learn · XGBoost · matplotlib/seaborn · Jupyter

*This is a learning project on a teaching dataset, not a clinical tool.*
