1. First project: LOADING DIGIT 
The target of this assignment is to load digits from 0,1,2,3,4,5,6,7,8,9 as we knew that it is Multiclassification dataset.
from this assignment i have chosen Randomforest, KNN, Decision Tree for compare the acuaracy rate of the result and noted that KNN provide better acuracy score which is 97.5%

2. Bitcoin Price Forcasting:
Data descrition:  it is multivariate time series data consist of Timestamp is epoch format, Open price of the day, Highest price of the day, Lowest price of the day, closing price of the day, volume of BTC transactived, volume in currency transactived and weighed price
Converting epoch time to Unix time and resampling to daily frequency as index
Clean data by checking NA value and used foreward filling fuction to fill null value
Decompose function to check stationarity of series by using Dickey-fuller or Box-Cox transformation and showing that data consist of Trend, Seasonality and Residual  
Modeling in this case i used Auto Arima to find the best P,D,Q and do model fitting and prediction.
Lastly, give an insight by visualize the prediction and conclusion.

4. Heart Disease UCI Prediction & Diagnosis
Using Logistic Regression Code by Hardik :) Dataset by Heart Disease UCI

Dataset Column Description: age in years sex (1 = male; 0 = female) cp chest pain type trestbps resting blood pressure (in mm Hg on admission to the hospital) chol serum cholestoral in mg/dl fbs (fasting blood sugar > 120 mg/dl) (1 = true; 0 = false) restecg resting electrocardiographic results thalach maximum heart rate achieved exang exercise induced angina (1 = yes; 0 = no) oldpeak ST depression induced by exercise relative to rest slope the slope of the peak exercise ST segment ca number of major vessels (0-3) colored by flourosopy thal Value 0: NULL (dropped from the dataset previously) Value 1: fixed defect (no blood flow in some part of the heart) Value 2: normal blood flow Value 3: reversible defect (a blood flow is observed but it is not normal)

target 1 or 0

Context: This database contains 76 attributes, but all published experiments refer to using a subset of 14 of them. In particular, the Cleveland database is the only one that has been used by ML researchers to this date. The "goal" field refers to the presence of heart disease in the patient. It is integer valued from 0 (no presence) to 4.

Table of contents
1)Imports & reading dataset

(2)Data Description

(3)Data Analysis

(4)Data Visualization

(5)Data Pre-processing

(6)Logistic Regression

(7)Conclusion

4. BANK MARKETING FIX DEPOSIT
   
TABLE OF CONTENT

I. DATA DESCRIPTION 

II. IMPORTING PACKAGE ANS DATA CLEANING 

III. EXPLORING DATA ANALYSIS 

IV. DATA PREMODELING 

V. DATA MODELING VI. 

CONCLUSION 

++++++++++++++++++++++++++++++++++++++++++ 

I.DATA DESCRIPTION The data is related with direct marketing campaigns of a Portuguese banking institution. The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be (or not) subscribed. There are two datasets: 1) bank-full.csv with all examples, ordered by date (from May 2008 to November 2010). 2) bank.csv with 10% of the examples (4521), randomly selected from bank-full.csv. The smallest dataset is provided to test more computationally demanding machine learning algorithms (e.g. SVM). The classification goal is to predict if the client will subscribe a term deposit (variable y). Number of Instances: 45211 for bank-full.csv (4521 for bank.csv) Number of Attributes: 16 + output attribute. Attribute information: Input variables: 1 - age (numeric) 2 - job : type of job (categorical: "admin.","unknown","unemployed","management","housemaid","entrepreneur","student","blue-collar","self employed","retired","technician","services") 3 - marital : marital status (categorical: "married","divorced","single"; note: "divorced" means divorced or widowed) 4 - education (categorical: "unknown","secondary","primary","tertiary") 5 - default: has credit in default? (binary: "yes","no") 6 - balance: average yearly balance, in euros (numeric 7 - housing: has housing loan? (binary: "yes","no") 8 - loan: has personal loan? (binary: "yes","no") 9 - contact: contact communication type (categorical: "unknown","telephone","cellular") 10 - day: last contact day of the month (numeric) 11 - month: last contact month of year (categorical: "jan", "feb", "mar", ..., "nov", "dec") 12 - duration: last contact duration, in seconds (numeric) 13 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact) 14 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric, -1 means client was not previously contacted) 15 - previous: number of contacts performed before this campaign and for this client (numeric) 16 - poutcome: outcome of the previous marketing campaign (categorical: "unknown","other","failure","success") Output variable (desired target): 17 - y - has the client subscribed a term deposit? (binary: "yes","no")

5. WEATHER FORCASTING

Collect the data and clean it.
Prepare visualization with respect to time vs. key feature.
Observe the stationarity of the series.
Develop charts to understand its nature.
Build the model – AR, MA, ARMA, and ARIMA.
Extract insights from prediction.
