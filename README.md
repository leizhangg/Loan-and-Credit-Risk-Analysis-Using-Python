In this notebook, I'll showcase how to conduct loan and credit risk analysis with Python.

- [Intoduction](#introduction)
   - [Problem Statement](#problem-statement)
   - [Objectives](#objectives)
   - [Dataset Overview](#dataset-description)
- [Data Wrangling](#data-wrangling)
- [Exploratory Data Analysis](#data-exploration-and-visualization)
   - [Loan Reason Distribution](#loan-reason)
   - [Loan Applicants' Occupation Distribution](#occupation)
   - [Loan Applicants' Working Years](#years-at-job)
   - [Derogatory Reports Distribution]

# Introduction
### Problem Statement:
One of our clients from credit risk department of a financial bank needs to investigate the reasons of customer loan default/delinquency and grow customer insights and develop business intelligence. For this purpose, a sample of about 10,663 loan customers is randomly selected from a huge customer database, and the key business factors, customer credit risk scores and loan performance information are collected for deep-dive risk analyses.
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
First, I want to know why are they applying for loan?

<p float="left">
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/performance.png" width="500" />
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/loan_reason_perfromace.png" width="500" />
</p>

In the sample dataset, 80.1% customers has good performance, and 19.9% of them has bad performance. Among applicants with Bad performance, 66% of them apply loan for Debt Consolidation, and 34% of them are for Home Improvement. 

Next, I want to know how much loan they applied for? Is there any difference of the loan request amount, mortgage due, property value, years at job and other numerical variables? I chose Boxplot to show the distribution of numerical data and skewness through displaying the min, quartiles, max and median.
<p align = "center">
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/boxplot_loan_due.png" />
</p>

The colored middle box in this graph represents the inter-quartile (IQR) and the line inside of the IQR represent the median of the data. The above boxplots show that:
   - The the midian, minimum, maxium and quartiles of Debt Consolidation with Bad Performance (Bad=1)is higher than those for Home Improvement. 
   - Applicants, who has Bad Performance (Bad=1) and apply for loan for Debt Consolidation, request more loan, have higer property value and mortgage due and longer years at job than thoes apply for Home Improvement.

Here, I used Chi-square Test to find out the association between Loan Reason and Performance. The null hypothesis is that there is no association between Loan Reason and Performance; and the alternative hypothesis is that there is an association. The p value of results is 0.96, which is greater than alpha value (0.05), thus we failed to reject the hypothesis and concluded that there is no association between Loan Reason and Performance. 
### Occupation
Next, I want to know what's there occupation, and does their occupation affect their performance?

<p align="left">
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/occupation_overall.png" width="400" />
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/occupation_by_performance.png" width="600" />
</p>

Occupation Ranking:   
Others > Professional/exe > Office people > Manager > Self employment > Sales
During each occupations, Sales have the largest proportion (36%) of loan applicants with Bad performance, and Self-employed comes the second, which is around 30%. Other and Manager share equal proportion, which is around 23%. The chi-square result shows that there is no association between occupation and performance. 

### Years at Job
Now we know that their occupation pattern and there is no association between occupation and performance. How about their working years? 
<p align="left">
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/yearAtJob_overall.png" width="500" />
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/yearAtJob_occupation_bar.png" width="500" />
</p>

Above charts illustrates that the number of loan applicants decreases as their working years increase. It implies that as people working longer, they have more money or have paid their loans. Accoridng to Chi-square test, there is no association between Years at job and performance.


For Derog report, Delinquent line, Trade line, File age, Inquiry and CR_score, I'm interested to know:
- What's the overall distribution of factors?
- What's the distribution of factors of applicant with Bad performance?
- Is there any association between factors and performance?

### Derog report /Delinquentline/Trade line/File age/Inquiry/CR_score distribution

<p align="left">
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/Derog%20Distribution%20overall.png" width="500" />
   <img src ="https://github.com/leizhangg/Loan-and-Credit-Risk-Analysis-Using-Python/blob/main/img/Derog%20Distribution%20by%20Performance.png" width="500" />
</p>

From above graphs, we can tell that 8,097 applicants (~86%) have 0 derogatory reports











