my graduation project in Epsilon AI Institute (kaggle competition)
![iStock-1026040678-e1565765520854](https://user-images.githubusercontent.com/59618586/123530752-499d1280-d6fe-11eb-9d5b-253e24ceaf26.jpg)

# Home-Credit-Risk :
Can you predict how capable each applicant is of repaying a loan?

# Overview :
https://www.kaggle.com/c/home-credit-default-risk

Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders.

Home Credit strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. In order to make sure this underserved population has a positive loan experience, Home Credit makes use of a variety of alternative data--including telco and transactional information--to predict their clients' repayment abilities.

While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data. Doing so will ensure that clients capable of repayment are not rejected and that loans are given with a principal, maturity, and repayment calendar that will empower their clients to be successful.

Inspired by some great kernels:
- sban: https://www.kaggle.com/shivamb/homecreditrisk-extensive-eda-baseline-0-772
- Will Koehrsen: 
    - https://www.kaggle.com/willkoehrsen/introduction-to-manual-feature-engineering 
    - https://www.kaggle.com/willkoehrsen/start-here-a-gentle-introduction
- [Aguiar[Updated 0.792 LB] LightGBM with Simple Features](https://www.kaggle.com/jsaguiar/updated-0-792-lb-lightgbm-with-simple-features/code)
- [Bojan TunguzXGB Simple Features](https://www.kaggle.com/tunguz/xgb-simple-features/code)
- [Ivan TimoshilovFork_LightGBM_with_Simple_Features](https://www.kaggle.com/znyksh/fork-lightgbm-with-simple-features)


# About the data :

### <font color='green'> Data frames we have are : </font>

#### <font color='purple'> application_{train|test}.csv </font>

* This is the main table, broken into two files for Train (with TARGET) and Test (without TARGET).
Static data for all applications. One row represents one loan in our data sample.

#### <font color='purple'> bureau.csv </font>

* All client's previous credits provided by other financial institutions that were reported to Credit Bureau (for clients who have a loan in our sample).
For every loan in our sample, there are as many rows as number of credits the client had in Credit Bureau before the application date.

#### <font color='purple'> bureau_balance.csv </font>

* Monthly balances of previous credits in Credit Bureau.
This table has one row for each month of history of every previous credit reported to Credit Bureau – i.e the table has (#loans in sample * # of relative previous credits * # of months where we have some history observable for the previous credits) rows.

#### <font color='purple'> POS_CASH_balance.csv </font>

* Monthly balance snapshots of previous POS (point of sales) and cash loans that the applicant had with Home Credit.
This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample * # of relative previous credits * # of months in which we have some history observable for the previous credits) rows.

#### <font color='purple'> credit_card_balance.csv </font>

* Monthly balance snapshots of previous credit cards that the applicant has with Home Credit.
This table has one row for each month of history of every previous credit in Home Credit (consumer credit and cash loans) related to loans in our sample – i.e. the table has (#loans in sample * # of relative previous credit cards * # of months where we have some 
history observable for the previous credit card) rows.

#### <font color='purple'> previous_application.csv </font>

* All previous applications for Home Credit loans of clients who have loans in our sample.
There is one row for each previous application related to loans in our data sample.

#### <font color='purple'> installments_payments.csv</font>

* Repayment history for the previously disbursed credits in Home Credit related to the loans in our sample.
There is a) one row for every payment that was made plus b) one row each for missed payment.
One row is equivalent to one payment of one installment OR one installment corresponding to one payment of one previous Home Credit credit related to loans in our sample.

#### <font color='purple'> HomeCredit_columns_description.csv </font>

* This file contains descriptions for the columns in the various data files.

![Annotation 2021-06-27 024230](https://user-images.githubusercontent.com/59618586/123530740-296d5380-d6fe-11eb-855f-e41f45be358b.png)

# files :
* Home credit risk.ipynb -> jupyter notebook of the whole project procedure
* finalized_model.sav -> model training you can load any time using pickle
* Project Presentation.pdf -> presentation of the whole procedure and the steps
