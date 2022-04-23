In this notebook, I'll showcase how to do loan and credit risk analysis with Python. The sensitive information and dataset has been modified.
# Introduction
### Problem Statement:
The credit risk department of a financial bank needs to investigate the reasons of customer loan default/delinquency and grow customer insights and develop business intelligence. For this purpose, a sample of about 10,663 loan customers is randomly selected from a huge customer database, and the key business factors, customer credit risk scores and loan performance information are collected for deep-dive risk analyses.
### Objectives:
Leanding loans to applicants who are likely to deafult is the largest source of risk losses. The objectives are:
- Distinguish financial customers by credit risk analysis
- Develop risk management strategies to mitigate risk losses (denying the loan, reducing the amount of loan,higer interest rate )

### Dataset Description:
| Variable | Description |
|----------|-------------|
|Client_ID | Unique Client ID|
|Loan_Request| Amount of loan request|
|MTG_Due| Dollar value due on current MTG
|Property_Value| Value of current property| 
|Loan_Reason| Home Improvement/Debt Consolidation|
|Occupation| Mgr, Office, Other, ProfEx, Sales, Self|
|Years_At_Job| Years at curretn job |
|Derog_Report| Number of derogatory reports |
|DELQ_Line| Number of delinquent tradelines |
|Trade_Line| Total number of trade lines |
|File_Age| Age of the oldest trade of a sonsumer (in months) |
|Inquiry| hard inquiry within last 12 months |
|Debt_Income_ Ratio| Debt/Income |
|CR_Score| Credit risk score |
|Bad| Performance indicator |

# Data Wrangling 
We want to make data-driven decisions. So the first step is to make sure the quality of data is usable, complete and reliable before it's analyzed and leveraged. During discovery of dataset, we found that this dataset is in good structure, but some numerical varibles are not in correct data format. There is no duplicates in the dataset, but a lot of missing values. As this dataset is small, deleting null values results in small dataset, so we will leave it. 

# Data Exploraitiona and Visualization
After cleaning the dataset, we want to find the 






