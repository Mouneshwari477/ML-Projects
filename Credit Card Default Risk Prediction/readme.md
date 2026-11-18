# Credit Card Default Risk Prediction
Predict payment default probability with calibrated evaluation and explicit responsible-lending limitations.

## Problem framing
Learning type: Supervised classification
Primary methods: logistic regression and random forests
Evaluation: macro F1 and class-level diagnostics
Decision boundary: Predictions support prioritization and review; they do not replace domain judgment.
Data: The notebook creates a deterministic, domain-shaped demonstration dataset locally. This keeps the project executable and avoids publishing private or questionably licensed data. The schema, target, caveats, and migration path to real data are documented in the notebook.

## Workflow
Reproducible environment and seed
Data contract and quality checks
Exploratory analysis
Leakage-safe or chronological split
Baseline and candidate-model comparison
Holdout metrics and diagnostics
Explainability or operational interpretation
Limitations, monitoring, and next steps

## Results
The notebook is committed with executed outputs. Open credit_card_default_risk.ipynb to inspect the actual model comparison, plots, holdout metrics, diagnostics, and sample predictions generated from the reproducible demo data.

## Technologies
Python
pandas and NumPy
scikit-learn
Matplotlib and Seaborn
Jupyter Notebook
