# CSET485 Assignment 1 — Report Template
**Student:** Udit Malik  
**Roll number:** S24CSEU0099  
**Dataset:** Adult Census Income  
**Random seed:** 99

> Complete this document only after running the notebook from top to bottom. Replace every bracketed instruction with your computed output. Do not submit unfilled placeholders or claim results that you have not verified.

## Data preprocessing
Describe dataset dimensions, target distribution, missing values, train/test split, numeric imputation and scaling, categorical imputation and encoding, and outlier policy. Include actual counts/percentages.

## Part 1 — OLS vs logistic regression
Report OLS test-prediction median, both thresholds, confusion matrix, mismatch count and percentage. Explain why OLS outputs are unbounded continuous values while logistic regression estimates probabilities bounded between zero and one.

## Part 2.1 — Simpson's paradox / subgroup effect
Compare the selected predictor's coefficient and confidence interval in the full, Female, and Male models. If there is no sign reversal, state what the estimates and uncertainty support. Do not claim Simpson's paradox without evidence. Explain possible policy consequences.

## Part 2.2 — Omitted-variable bias
State the omitted variable (`education_num`). Include at least four predictors with full/reduced coefficients and percentage changes from `reports/part2_2_omitted_variable.csv`. Identify the largest shift and explain why coefficient changes show model sensitivity rather than proving causality.

## Part 2.3 — Adversarial subset
Report the count and percentage of confident incorrect predictions. Compare the subset with the full test set using age and sex distributions. Explain plausible failure mechanisms without assuming patterns the data do not show.

## Part 2.4 — Fairness trade-offs
Include the threshold table and `reports/fairness_tradeoff.png`. Define Group A as Female and Group B as Male. Explain ratio direction, undefined values, and limits of demographic parity, equalized odds, and predictive parity. Calculate a concrete trade-off using actual values.

## Part 3 — Descriptive analysis questions
Write approximately 250–300 words for each answer and cite your own notebook results.

### 1. Threshold-based versus direct logistic classification
[Discuss mismatch count/percentage and OLS median.]

### 2. Subgroup effects
[Discuss full/Female/Male coefficients and confidence intervals.]

### 3. Omitted-variable test
[Insert a table with at least four predictors and before/after coefficients.]

### 4. Detecting a hidden confound
[Propose a concrete method such as external validation plus a domain-expert audit; explain how it would be carried out.]

### 5. Adversarial subset
[Discuss observed subset characteristics and how the fitted model could fail confidently.]

### 6. Fairness trade-off in a real-person scenario
[Use actual group rates and at least two thresholds to describe who is affected.]

### 7. Defend a specific threshold
[Use at least three computed metrics and acknowledge the strongest counterargument.]

### 8. Demographic parity versus equalized odds
[Make a recommendation grounded in the computed fairness table and state which metric is sacrificed.]

## Part 4 — Reflection (approximately 500 words)
Recommend deployment, conditional deployment, or rejection. Explain why a single score is insufficient, using at least three limitations supported by computed results. Reflect on transparency, uncertainty, and fairness trade-offs.

## Reproducibility checklist
- [ ] Notebook runs from top to bottom without errors.
- [ ] Dataset source and preprocessing are documented.
- [ ] Every numerical claim in the report can be regenerated.
- [ ] Tables and fairness chart are included.
- [ ] No placeholders remain.
- [ ] PDF report exported and reviewed.
