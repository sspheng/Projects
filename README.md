1. First project: LOADING DIGIT 
The target of this assignment is to load digits from 0,1,2,3,4,5,6,7,8,9 as we knew that it is Multiclassification dataset.
from this assignment i have chosen Randomforest, KNN, Decision Tree for compare the acuaracy rate of the result and noted that KNN provide better acuracy score which is 97.5% 
2. Bitcoin Price Forcasting: Box-Cox Transformations
df_daily['Cln_Weighted_Price'], lmbda = stats.boxcox(df_daily.Cln_Weighted_Price)

??stats.boxcox
print("Dickey–Fuller test: p=%f" % sm.tsa.stattools.adfuller(df_daily.Cln_Weighted_Price)[1])

print(sm.tsa.stattools.adfuller(np.log(df_daily.Cln_Weighted_Price))[1])

 
 
Resampling to monthly frequency
df_month = df.resample('M').mean()

Resampling to annual frequency
df_year = df.resample('A-DEC').mean()

Resampling to quarterly frequency
df_Q = df.resample('Q-DEC').mean()

PLOTS
fig = plt.figure(figsize=[15, 7]) plt.suptitle('Bitcoin exchanges, mean USD', fontsize=22)

plt.subplot(221) plt.plot(df.Weighted_Price, '-', label='By Days') plt.legend()

plt.subplot(222) plt.plot(df_month.Weighted_Price, '-', label='By Months') plt.legend()

plt.subplot(223) plt.plot(df_Q.Weighted_Price, '-', label='By Quarters') plt.legend()

plt.subplot(224) plt.plot(df_year.Weighted_Price, '-', label='By Years') plt.legend()

plt.tight_layout()
plt.show()

df = df.resample('M').mean() df[df["Weighted_Price"].isna()] df["Int_Weighted_Price"] = df["Weighted_Price"].ffill() df["New_Weighted_Price"] = df["Int_Weighted_Price"].rolling(window=4).mean() import numpy as np

df["Cln_Weighted_Price"] = np.where(df["Weighted_Price"].isnull(),df["Int_Weighted_Price"],df["Weighted_Price"])

df_monthly=df

plt.figure(figsize=[20,10]) decomp_viz = sm.tsa.seasonal_decompose(df.Cln_Weighted_Price)

fig = decomp_viz.plot() fig.set_size_inches((16, 9))

Tight layout to realign things
fig.tight_layout() plt.show()

print("Dickey–Fuller test: p=%f" % sm.tsa.stattools.adfuller(df.Cln_Weighted_Price)[1]) plt.show()

Box-Cox Transformations
df_monthly['Cln_Weighted_Price'], lmbda = stats.boxcox(df_monthly.Cln_Weighted_Price)

print("Dickey–Fuller test: p=%f" % sm.tsa.stattools.adfuller(df.Cln_Weighted_Price)[1]) plt.show()

# make an in-sample forecast
from pandas import read_csv
from pandas import to_datetime
from pandas import DataFrame
from matplotlib import pyplot
from fbprophet import Prophet

uber- ORBIT
XGBOOST
Neural networks
load data
path = 'https://raw.githubusercontent.com/jbrownlee/Datasets/master/monthly-car-sales.csv' df = read_csv(path, header=0)

prepare expected column names
df.columns = ['ds', 'y'] df['ds']= to_datetime(df['ds'])

define the model
create test dataset, remove last 12 months
train = df.drop(df.index[-12:]) print(train.tail())

model = Prophet()

fit the model
model.fit(df_monthly)

define the period for which we want a prediction
future = list() for i in range(1, 13): date = '1968-%02d' % i future.append([date])

future = DataFrame(future) future.columns = ['ds'] future['ds']= to_datetime(future['ds'])

use the model to make a forecast
forecast = model.predict(future)

summarize the forecast
print(forecast[['ds', 'yhat', 'yhat_lower', 'yhat_upper']].head())

plot forecast
model.plot(forecast) pyplot.show()
3. Heart Disease UCI Prediction & Diagnosis
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
