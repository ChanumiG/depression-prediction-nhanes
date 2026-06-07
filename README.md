# Depression Prediction Using Machine Learning: Findings from NHANES 2021–2023

## Abstract
### Background
Depression affects approximately 332 million people globally and remains substantially underdiagnosed, with only one third of affected individuals receiving treatment. Machine learning (ML) offers a complementary approach to traditional screening by identifying individuals at elevated risk using non-laboratory health and socioeconomic data.
### Methods
This study utilised data from the National Health and Nutrition Examination Survey (NHANES) 2021–2023 to predict depression (PHQ-9 ≥10) in 5,455 adults. Two supervised ML algorithms were compared: Logistic Regression and Random Forest. Candidate predictors spanning sociodemographic, socioeconomic, lifestyle and clinical domains were selected through a three-stage feature selection pipeline comprising missingness filtering, correlation-based removal and Logistic LASSO. Models were trained using an 80/20 stratified train-test split with class weighting. Performance was evaluated using ROC-AUC, PR-AUC, sensitivity, specificity, precision, F1 score and accuracy. Model interpretation was performed using odds ratios and permutation importance, whilst fairness was assessed across sex and age subgroups.
### Results 
Both models demonstrated moderate and comparable discriminative ability, achieving ROC-AUC values of 0.758 (95% CI: 0.718–0.798) for Logistic Regression and 0.760 (95% CI: 0.723–0.798) for Random Forest. DeLong’s test confirmed no significant difference between models (p = 0.962). Logistic Regression achieved higher sensitivity (0.628 vs 0.531), identifying a greater proportion of depressed individuals. Food insecurity and younger age emerged as the most influential predictors of depression. Performance was comparable between males and females but varied across age groups, with both models performing worst among adults aged 18–35 years.
### Conclusions: 
Both models achieved moderate discrimination using only variables obtainable without laboratory investigation. These findings suggest clinically useful depression risk stratification may be achievable using readily obtainable health and socioeconomic data. Logistic Regression may be preferable for screening applications due to its higher sensitivity and greater interpretability. Further external validation would be required.

## Dataset
Data sourced from NHANES 2021–2023 (Cycle L), available at:
[https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023]

Data downloads automatically when the notebook is run, no manual download required.

## How to Reproduce
1. Open the notebook in Google Colab
2. Run all cells top to bottom (Runtime → Restart session and run all)
3. Data downloads automatically from the CDC URL above
4. All outputs, figures, and tables will be generated automatically

## Dependencies
- Python 3.12
- pandas 2.2.2
- numpy 2.0.2
- scikit-learn 1.6.1
- scipy 1.16.3
- matplotlib 3.10.0
- seaborn 0.13.2
