# What Drives High Medical Costs?

## Business Problem
A health insurance actuary wants to identify which patient factors 
best predict high medical charges to improve the underwriting model.

## Tools Used
- Python (pandas, seaborn, matplotlib, scikit-learn)
- Jupyter Notebook

## Dataset
- Source: Kaggle — Medical Cost Personal Dataset
- 1,338 rows | 7 columns

## Key Findings
- Smoking status is the strongest predictor (correlation: 0.79 with charges)
- Smokers pay ~4x more than non-smokers (median $34K vs $7K)
- Single-feature model (smoker only) R² = 0.66
- Multi-feature model (age + BMI + smoker + children) R² = 0.78
- Region has minimal impact on charges

## Recommendations
1. Flag smoker status as highest-risk variable in premium pricing
2. Apply BMI thresholds — patients with BMI > 30 warrant higher risk tiers
3. Age-based tiering supports stepped premium bands

## Files
- `notebook/insurance_cost_analysis.ipynb` — full analysis notebook
