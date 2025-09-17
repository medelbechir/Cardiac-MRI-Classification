# Cardiac MRI Classification — Kaggle (1st place)

Solution to the **IMA205 Kaggle Challenge**: classification of cardiac pathologies from MRI scans and partial segmentations.

## Highlights
- 🏆 **1st place** on the Kaggle private leaderboard — 49/50 correct predictions
- Complete end-to-end pipeline: Left Ventricle (LV) reconstruction → feature engineering → stacked machine-learning models

## Pipeline
1. **Left Ventricle Reconstruction** (`notebooks/VG_Reconstruction.ipynb`)
   Compared UNet2D, active contours and **morphological filling** (Dice ≈ 0.99).

2. **Feature Engineering** (`notebooks/Feature_Model_Testing.ipynb`)
   34 anatomical & functional features: volumes, ejection fractions, myocardial thickness, contraction dynamics.

3. **Classification** (`notebooks/Final_Pipeline.ipynb`)
   Random Forest baseline → specialized Gradient Boosting & XGBoost for fine discrimination of classes 1 & 2.
   Dynamic aggregation of predictions for optimal accuracy.

## Results
| Phase    | Model                    | Accuracy |
|----------|---------------------------|----------|
| Baseline | Random Forest (34 feats)  | 95%      |
| Final    | RF + GB + XGBoost         | **98%**  |

## Repository structure
```
notebooks/   - Jupyter notebooks for each stage
report/      - Full PDF report
results/     - Final Kaggle submission
```

## Quick start
```bash
git clone https://github.com/medelbechir/Cardiac-MRI-Classification.git
cd Cardiac-MRI-Classification
pip install -r requirements.txt
```

## Dependencies
Python 3.x with:
```
numpy
pandas
scikit-learn
xgboost
optuna
matplotlib
nibabel
```

## Full report
See [`report/Rapport_Challenge_Kaggle.pdf`](report/Rapport_Challenge_Kaggle.pdf) for detailed methods and analyses.

## Author
Mohamed Mohamed El Bechir  
[GitHub](https://github.com/medelbechir) · [LinkedIn](https://www.linkedin.com/in/mohamed-el-bechir-6958a5242/)
