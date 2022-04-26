In this notebook, I'll showcase how to conduct loan and credit risk analysis with Python.
- [Intoduction](#introduction)
   - [Problem Statement](#problem-statement)
   - [Objectives](#objectives)
   - [Dataset Overview](#dataset-description)
- [Data Wrangling](#data-wrangling)
- [Exploratory Data Analysis](#data-exploration-and-visualization)
- 

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
|Bad| Performance indicator, 1=Bad (90 days past due), 0=Good |

# Data Wrangling 
We want to make data-driven decisions. So the first step is to make sure the quality of data is usable, complete and reliable before it's analyzed and leveraged. During discovery of dataset, we found that this dataset is in good structure, but some numerical varibles are not in correct data format. There is no duplicates in the dataset, but a lot of missing values. As this dataset is small, deleting null values results in small dataset, so we will leave it null. 

# Data Exploration and Visualization
This step is also known as Exploratory Data Analysis, or EDA. During this process, we will investigate the dataset to discover pattern, form hppotheses based on our understanding of the dataset, and generate summary statistics and visualizations to understand the data better. 

### Loan Reason 
First, we want to know why are they applying for loan?

<p float="left">
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/performance.png" width="500" />
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/loan_reason_perfromace.png" width="500" />
</p>

In the sample dataset, 80.1% customers has good performance, and 19.9% of them has bad performance. Among applicants with Bad performance, 66% of them apply loan for Debt Consolidation, and 34% of them are for Home Improvement. 


