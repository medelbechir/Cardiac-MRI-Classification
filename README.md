# Cardiac MRI Classification — Kaggle (1st place)

Solution to the **IMA205 Kaggle Challenge**: classification of cardiac pathologies from MRI scans and partial segmentations.

## Highlights
- 🏆 **1st place** on the private leaderboard — 49/50 correct predictions
- Complete end-to-end pipeline: LV reconstruction → feature engineering → stacked ML models

## Pipeline
1. **Left Ventricle Reconstruction** (`notebooks/VG_Reconstruction.ipynb`)
   - Compared UNet2D, active contours and **morphological filling** (Dice ≈ 0.99).
2. **Feature Engineering** (`notebooks/Feature_Model_Testing.ipynb`)
   - 34 anatomical & functional features: volumes, ejection fractions, myocardial thickness, contraction dynamics.
3. **Classification** (`notebooks/Final_Pipeline.ipynb`)
   - Random Forest baseline → specialized Gradient Boosting & XGBoost for fine discrimination of classes 1 & 2.
   - Dynamic aggregation of predictions for optimal accuracy.

## Results
| Phase        | Model                    | Accuracy |
|--------------|---------------------------|----------|
| Baseline     | Random Forest (34 feats)  | 95%      |
| Final        | RF + GB + XGBoost         | **98%**  |

## Repository structure
