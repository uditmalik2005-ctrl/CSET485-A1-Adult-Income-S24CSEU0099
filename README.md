# CSET485 Assignment 1 — Adult Census Income

**Student:** Udit Malik  
**Roll number:** S24CSEU0099  
**Course:** CSET485 — AI and Society

A reproducible, notebook-based analysis of the UCI Adult Census Income dataset for Assignment 1. It includes model comparison, subgroup analysis, omitted-variable sensitivity, confident-error analysis, and fairness metrics.

## Assignment mapping

| Requirement | Notebook section / output |
|---|---|
| Preprocessing and 70/30 split | Notebook sections 1; fixed `random_state=99` |
| OLS vs logistic threshold comparison | Part 1; `reports/part1_predictions.csv` |
| Subgroup coefficient comparison | Part 2.1; `reports/part2_1_subgroup_coefficients.csv` |
| Omitted-variable stress test | Part 2.2; `reports/part2_2_omitted_variable.csv` |
| Confident incorrect predictions | Part 2.3; `reports/part2_3_adversarial_subset.csv` |
| Fairness threshold sweep | Part 2.4; `reports/part2_4_fairness_thresholds.csv` and `reports/fairness_tradeoff.png` |
| Summary metrics | `reports/summary_metrics.csv` |
| Written report framework | `REPORT_TEMPLATE.md` |

## Dataset and seed

The supplied brief assigns Adult Census Income to roll numbers ending in 6, 7, 8, or 9. S24CSEU0099 ends in 9; its last three digits are 099, so the split uses `random_state=99` with 70% training and 30% testing.

The notebook downloads the UCI Adult dataset when run. It treats `?` as missing, imputes numeric values with the training-set median, imputes categorical values with the training-set most frequent category, standardizes numeric variables, and one-hot encodes categorical variables.

## Project layout

```text
CSET485-A1-Adult-Income-S24CSEU0099/
├── README.md
├── REPORT_TEMPLATE.md
├── requirements.txt
├── .gitignore
├── notebooks/CSET485_A1_Udit_Malik.ipynb
├── reports/README.md
└── src/README.md
```

## Run locally

```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter lab
```

Open `notebooks/CSET485_A1_Udit_Malik.ipynb` and run all cells from top to bottom. Internet access is required to download the dataset. You can also upload the notebook to Google Colab and run it there.

After execution, use the generated tables and chart to complete `REPORT_TEMPLATE.md`. Do not submit unfilled placeholders or claim results that have not been verified. Simpson's paradox and fairness conclusions must be supported by actual output.

## References

- UCI Machine Learning Repository, Adult dataset: https://archive.ics.uci.edu/ml/machine-learning-databases/adult/
- Course assignment instructions supplied by the student.
