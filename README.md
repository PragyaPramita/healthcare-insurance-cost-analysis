# What Drives High Medical Costs?

## Business Problem
A health insurance actuary wants to identify which patient factors 
best predict high medical charges to improve the underwriting model.

## Tools Used
- Python (pandas, seaborn, matplotlib, scikit-learn, scipy)
- Jupyter Notebook

## Dataset
- Source: Kaggle — Medical Cost Personal Dataset
- 1,338 rows | 7 columns

## Key Findings
- Smoking status is the dominant cost predictor (feature importance: 62%)
- Smokers pay ~4x more than non-smokers ($32,050 vs $8,434 average)
- Difference is statistically significant (t-test: t=46.67, p<0.0001)
- BMI is the second most important feature (23% importance)
- Region and sex have minimal impact on charges

## Model Results
| Model | R² (5-Fold CV) | RMSE |
|---|---|---|
| Linear Regression | 0.7469 | $6,072 |
| Ridge Regression | 0.7469 | $6,072 |
| **Random Forest** | **0.8254** | **$5,025** |

Random Forest outperforms linear models by 8 R² points and reduces 
prediction error by $1,047 per patient.

## Business Recommendations
1. Smoker status must be the primary variable in premium pricing
2. BMI-based risk tiers (especially above 30) should be implemented
3. Age-stepped premium bands are statistically justified
4. Region and sex can be deprioritized in underwriting models

## Files
- `notebook/insurance_cost_analysis.ipynb` — full analysis notebook
