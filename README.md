# Credit-EDA-Case-Study

**Introduction**

This case study aims to give you an idea of applying EDA in a real business scenario. In this case study, apart from applying the techniques that you have learnt in the EDA module, you will also develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.

 

**Business Understanding**

The loan providing companies find it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it as their advantage by becoming a defaulter. Suppose you work for a consumer finance company which specialises in lending various types of loans to urban customers. You have to use EDA to analyse the patterns present in the data. This will ensure that the applicants are capable of repaying the loan are not rejected.

 

When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:

If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company

If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company.

 

The data given below contains the information about the loan application at the time of applying for the loan. It contains two types of scenarios:

The client with payment difficulties: he/she had late payment more than X days on at least one of the first Y instalments of the loan in our sample,

All other cases: All other cases when the payment is paid on time.

 

 

When a client applies for a loan, there are four types of decisions that could be taken by the client/company):

Approved: The Company has approved loan Application

Cancelled: The client cancelled the application sometime during approval. Either the client changed her/his mind about the loan or in some cases due to a higher risk of the client he received worse pricing which he did not want.

Refused: The company had rejected the loan (because the client does not meet their requirements etc.).

Unused offer:  Loan has been cancelled by the client but on different stages of the process.

In this case study, we will use EDA to understand how consumer attributes and loan attributes influence the tendency of default.

 

 

**Business Objectives**

This case study aims to identify patterns which indicate if a client has difficulty paying their installments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study.

 

In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default.  The company can utilise this knowledge for its portfolio and risk assessment.


**Dataset**

We have 3 types of datasets: 

1. 'application_data.csv'  contains all the information of the client at the time of application.
The data is about whether a client has payment difficulties.

2. 'previous_application.csv' contains information about the client’s previous loan data. It contains the data whether the previous application had been Approved, Cancelled, Refused or Unused offer.

3. 'columns_description.csv' is data dictionary which describes the meaning of the variables.

Please click on this link to find the dataset: https://drive.google.com/drive/folders/1HsVEiU37kFPV8mF8Z1fqL39t3dPzIPzq?usp=share_link


**Solution**

After doing extensive univariate, and bivariate analysis, on all the 
columns of the provided dataset, we came across following patterns:
Results of Univariate analysis of categorical columns:

• If the credit amount of the client loan is in the range (43239-749394), 
then there is high probability that client will have payment difficulties.

• Client whose Loan Annuity is in the range (43141-70582) are less 
likely to default on their loan.

• Client's whose permanent address does not match contact address 
are more likely to default.

• Client’s who stay in the region rated as 2nd and 3rd are highly likely to 
default on their payments.

• Client’s whose permanent address does not match with work address 
are more prone to default.

• More percentage of males default as compared to females.

• Under column - How many days before the application the person 
started current employment- A lot of clients have put 365243 
number. Further investigation is needed to find the root cause. 

Results of Univariate analysis of numerical columns:

• If ‘EXT_SOURCE_2’, ‘EXT_SOURCE_3’ i.e. Normalized score from 
external data sources is less, of clients is less, then clients are likely to 
have payment related issues.

• If number of enquiries to Credit Bureau about the client one day year 
(excluding last 3 months before application) are more then 3, then 
there is higher possibility of default.

Results of Bivariate analysis:

• If value of ‘AMT_REQ_CREDIT_BUREAU_QRT’ (Credit Bureau 
enquiries) oscillates between (0.00 - 0.25), and the 
AMT_INCOME_TOTAL (Income of client) is in range (707130.0, 
877500.0], then client is more likely to default on payment.

• If AMT_CREDIT (Credit amount of the loan) is in range (43239.015, 
397197.0], and CNT_FAMILY_Members (Count of Family members) > 
3 then there is more probability that client will default.

• If AMT_REQ_CREDIT_BUREAU_YEAR is greater then 3, and 
AMT_CREDIT in range (749394.0, 1101591.0], then client is less likely 
to default.

• If Count of children > 0, and DAYS_REGISTRATION (How many days 
before the application did client change his registration) is in range –
(9331.8 - 6221.2], then client is more likely to default.

• If CNT_FAMILY_Members > 2, and NAME_HOUSING_TYPE is 
Municipal apartment, then client is more likely to default.

• If AMT_REQ_CREDIT_BUREAU_YEAR (Credit bureau enquiries) > 5, 
and NAME_HOUSING_TYPE is Office apartment, then client is likely to 
default.

Numeric variable Correlations:

• EXT_SOURCE_3 positively correlates with 
AMT_REQ_CREDIT_BUREAU_HOUR, 
AMT_REQ_CREDIT_BUREAU_DAY, AMT_REQ_CREDIT_BUREAU_WEEK 
when client faces payment difficulties, otherwise, it negatively 
correlates.

• AMT_REQ_CREDIT_BUREAU_YEAR negatively correlates with 
AMT_REQ_CREDIT_BUREAU_HOUR,AMT_REQ_CREDIT_BUREAU_DAY 
and AMT_REQ_CREDIT_BUREAU_WEEK when client faces difficulty, 
otherwise it correlates positively
