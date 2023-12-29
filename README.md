# Loan Default Prediction
Problem Defined:
The problem is to predict personal loan defaults using a dataset of 10,000 personal loan records.

Data Preparation:
- Started with 10,000 personal loan records.
- Performed data cleaning to handle missing values through imputation and deletion, resulting in a final count of 9,997 credit records.
- Applied feature engineering and encoding for discrete variables to transform the original 21 independent variables into 70 variables through discretization.

Data Process:
- Split the data into test and training sets.
- Used Sequential Backward Selection (SBS) and Recursive Feature Elimination (RFE) to perform dimensionality reduction on a subset of the training sample, ultimately retaining 23 independent variables. The overlap of independent variables selected by the two methods was 65%.
- Fitted the subset of the training sample using three types of models: Logistic Regression, Bayesian, and Decision Tree.
- Performed parameter tuning on the remaining samples in the training set.

Data Analysis:
- Used the trained models to predict the default situation in the test samples. It was found that using the Bayesian model to predict the results under the condition of unscreened independent variables was the best, with the optimal recall rate reaching 0.932 and a low precision of 0.414.
