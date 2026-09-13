# 💳 Loan Default Prediction and Profit-Aware Model Selection

## 💼 Business Use Case

Credit-risk modeling is ultimately a decision problem, not just a classification exercise. A lender needs to identify applicants with elevated default risk without rejecting so many reliable borrowers that profitable business is lost.

This project compares several classification approaches and evaluates them through both predictive performance and a simplified profit framework, bringing model selection closer to the economics of an actual lending decision.

## 🎯 Principal Objective

The objective is to estimate loan-default risk, compare interpretable and higher-capacity models, and evaluate how the classification threshold changes the financial outcome of the decision process.

The notebook progresses from logistic regression to decision trees and XGBoost, while keeping the business payoff assumptions visible throughout the comparison.

## 🔍 Key Takeaways

Under the payoff assumptions used in the notebook, the **pruned decision tree produces the highest displayed test profit per applicant at $161.82**, compared with **$153.41** for multivariable logistic regression and **$145.35** for XGBoost. The result is a useful reminder that the most complex model is not necessarily the best choice once business value and interpretability are considered together.

The experiment also shows why a default 0.50 cutoff may be inappropriate in credit risk. The cost of approving a future defaulter can be very different from the cost of declining a safe borrower, so threshold selection should be tied to expected value rather than convention alone.

A production lending model would require richer economics, probability calibration, out-of-time validation, fairness testing, explainability, drift monitoring, and strong governance before it could support real credit decisions.

## 💻 Explore the Notebook

The [notebook](https://github.com/saels/loan-default-prediction/blob/2f255ae90ad534ef3958b49918dee2a9fd5436ef/Loan_default_prediction.ipynb) contains the full model comparison, threshold analysis, pruning process, and profit evaluation. Check the code to see how predictive results are translated into business decisions and how the same framework can be extended with more realistic lending economics.
