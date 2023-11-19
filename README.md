# Developing credit risk model-Building PD Model
# Introduction

Welcome to my project. Before I get into the details of my project,  let's take a quick look at what credit risk is and why it holds significance.

In general, when giving credit a lender, provides goods and services to a debtor or a borrower based on the trust that the borrower will repay the lender at some point in the future ,in exchange for providing the goods or services to the borrower in the present, the lender receives a payment which is called interest.The most common type of loan provided by lenders to borrowers ,is money. forexample Credit cards and home ownership loans are two very good examples of credit provided by lenders. This money is not yours and you are required to repay the respective sum to the bank.Typically, you have to repay with interest.And this is how the bank makes a profit.

The likelihood that a borrower would not repay their loan to the lender is called credit risk.

In this case, the lender would not receive the owed principal. Moreover, they wouldn't be paid the interest  and therefore they  will  suffer a substantial loss. The event of a borrower being unable to make the required payments to repay their debt is called default.To protect themselves against borrower defaults, lenders must assess the credit risk associated with each borrower very well.

There are lots of way that lender cover the its risk for high risk borrowers:such as collaterals or increasing interst rate.No matter which type of strategy the borrower would decide to pursue, What's most important is to be able to estimate credit risk of each borrower as precisely as possible.Lending to borrowers with a high probability of default is one of the main reasons for serious financial crises.


Lenders know that there is a certain amount of credit risk associated with every borrower.They expect that there could be a loss when lending to any borrower. Such expected loss comes at a result of different types of factors such as Borrower specific factors and The economic environment and the combination of the two.Lenders may face other unforeseen losses because of the economic environment such as unexpected loss and exponential losses.
Expected loss or EL is associated with credit risk.Expected loss is the amount a lender might lose by lending to a borrower and it has a of three components: probability of default ,loss given default and exposure at default.

Lenders should build different statistical models to estimate each of these components and then multiply them
to obtain the expected loss . My project is focous on Probability of default or PD which means the likelihood that a borrower would not be able or would not be willing to repay their debt in full or on time. 

just simple explanition of two other componet,LGD It is the proportion of the total exposure that cannot be recovered by the lender once default hasoccurred and EDA is the maximum that a bank may lose when a borrower defaults on a loan. Let's build the model together!


Important definition

- Default: The event of a borrower being unable to make the required payments to repay their debt is called default.
- EL:Expected loss is the amount a lender might lose by lending to a borrower.
- Component of EL :PD*LGD*EAD


Goal of the project
- Predict the probability of the default.  

Dataset 
- Main dataset is stored in MySQL database ==>loan_data_bank.csv===> Quality_Check_Data_Preprocessing.ipynb
-clean_data.csv===> for Credit _Risk_Modelling.ipynb
-loan_data_2015===> Unseendata 
- Dictionary of the datasets.
The link that you can have a direct access to datasets:
https://drive.google.com/file/d/1fm_Tgn6peNfo0RmX-l56LqwDBzf30ZfQ/view?usp=drive_link

Tableau Public link
This is the link : https://public.tableau.com/app/profile/parinaz.mohammadi/viz/Insighttodatasetofcreditriskmodelling/Dashboard1?publish=yes

Notebooks
- You can find Quality data cheack and data Preprocessing  in the Quality_Check_Data_Preprocessing.ipyn and I saved it as "clean_data.csv"
- You can find Modelling process in Credit _Risk_Modelling.ipynb

Dictionary of the data for final 21 features

- loan_amnt: The listed amount of the loan applied for by the borrower. If at some point in time, the credit department reduces the loan amount, then it will be reflected in this value.
- term: The number of payments on the loan. Values are in months and can be either 36 or 60.
- int_rate: Interest Rate on the loan	
- grade: loan grade	
- sub_grade: loan subgrade
- emp_length: Employment length in years. Possible values are between 0 and 10 where 0 means less than one year and 10 means ten or more years. 
- home_ownership: The home ownership status provided by the borrower during registration. Our values are: RENT, OWN, MORTGAGE, OTHER. 	
- verification_status: Indicates if the co-borrowers' joint income was verified by LC, not verified, or if the income source was verified
- loan_status :Current status of the loan	
- purpose	
- delinq_2yrs :The number of 30+ days past-due incidences of delinquency in the borrower's credit file for the past 2 year	
- inq_last_6mths: The number of inquiries in past 6 months (excluding auto and mortgage inquiries)
- revol_bal: Total credit revolving balance
- revol_util: Revolving line utilization rate, or the amount of credit the borrower is using relative to all available revolving credit.	
- total_acc : The total number of credit lines currently in the borrower's credit file	
- out_prncp: Remaining outstanding principal for total amount funded
- total_rec_late_fee : Late fees received to date
- last_pymnt_amnt : last_pymnt_amnt	
- dti_bins_encoder: A ratio calculated using the borrower’s total monthly debt payments on the total debt obligations,  divided by the borrower’s self-reported monthly income- I changed to the bin and then covert it ito dummy by labelencoder
- annual_inc_bins_encoder: The self-reported annual income provided by the borrower during registration- I changed to the bin and then covert it ito dummy by labelencoder
- good bad: default borrower=0 non-default=1

My approach 
- Data quality check
- Preprossing the data such as log-transformation ,quantile cut.
- Spiliting data To X and y(target)-then spilit to tarian and test
- Normalization
- Convert to dummy variable
- Bulid the classification model and KNN
- Compare them 
- Evaluate the performance
- Handling imbalance dataset
- Feed the model with unseendataset


```python

```
