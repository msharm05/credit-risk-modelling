# Credit Risk Modelling

## Probability of loan default (PD) prediction using financial data.

Credit risk modelling is a crucial task in the banking domain. It involves estimating the likelihood of a borrower to default a loan. Predicting the probability of loan default enables banks to make intelligent decisions related to money lending. It aslo helps to understand and gain insights on factors that drive loan defaults. For a given borrower, the probability of loan default is estimated using several financial attributes such as income, credit rating, pervious debts, number of dependents etc. With the help of machine learning, PD can be determined very accurately and is already being used by a number of banking institutions across the world.

## Objective

The objective of this project was to build a machine learning model that can predict PD for a given borrower using its financial attributes.

## Dataset

The dataset used in this project is comprised of financial data of 10000 different borrowers. Each record (borrower) has 15 different financial attributes (features) named X1 to X15. There is no background information available on these features. The data type of ecah feature is listed below:-

|Feature|Description|
|---|---|
|X1|Categorical, 3 Categories|
|X2|Numeric, Missing values|
|X3|Numeric|
|X4|Numeric, Missing values|
|X5|Numeric|
|X6|Numeric|
|X7|Numeric|
|X8|Numeric|
|X9|Numeric|
|X10|Numeric|
|X11|Numeric|
|X12|Numeric|
|X13|Categorical, 3 Categories|
|X14|Categorical, 5 Categories|
|X15|Categorical, 2 Categories|
|Deafult_Ind (Class Label) : Non-Default, Default|

The class distribution of the dataset is extremely imbalanced.

| Class Label | No. of Records | Percentage |
|---|---|---|
|Non-Default|9871|98.71%|
|Default|129|1.29%|

The first 7000 records are used as the train set and the remaining 3000 as the test set.

There are two files in the **CODE_dr** folder:-
1. financial_data.csv
2. default_data.csv

**financial_data.csv** contains financial attributes (X1-X15) of 10000 borrowers along with a unique **LOAN_ID** for each borrower.

**default_data.csv** contains **LOAN_ID**(s) of borrowers with loan default.

## Results

The performance of the model was evaluated on the test set using F1-score and area under the Precision-Recall curve as the evaluation metrics. The results have been summarized in the table below:-

|Class Label|Precision|Recall|F1-score|AUC PR|
|---|---|---|---|---|
|Non-Default|99.93|99.86|99.90|-|
|Default|90.24|94.87|92.50|-|
|Average|95.09|97.37|**96.20**|**95.08**|

