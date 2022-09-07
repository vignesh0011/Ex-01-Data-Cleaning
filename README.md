# Ex-01_DS_Data_Cleansing
# AIM
To read the given data and perform data cleaning and save the cleaned data to a file.

# Explanation
Data cleaning is the process of preparing data for analysis by removing or modifying data that is incorrect ,incompleted , irrelevant , duplicated or improperly formatted. Data cleaning is not simply about erasing data ,but rather finding a way to maximize datasets accuracy without necessarily deleting the information.

# ALGORITHM
## STEP 1
Read the given Data

## STEP 2
Get the information about the data

## STEP 3
Remove the null values from the data

## STEP 4
Save the Clean data to the file

# CODE
~~~
Developed by: M VIGNESH
Reg.no: 212220233002
~~~

## Data_set.csv
~~~
import numpy as np
import pandas as pd
import io
from google.colab import files
uploaded = files.upload()
dd = pd.read_csv(io.BytesIO(uploaded['Data_set.csv']))
print(dd)
dd.tail()
dd.info()
dd.isnull()
dd.isnull().sum()
#mode
dd['show_name'] = dd['show_name'].fillna(dd['aired_on'].mode()[0])
dd['aired_on'] = dd['aired_on'].fillna(dd['aired_on'].mode()[0])
dd['original_network'] = dd['original_network'].fillna(dd['aired_on'].mode()[0])
dd.head()
#mean
dd['rating'] = dd['rating'].fillna(dd['rating'].mean())
dd['current_overall_rank'] = dd['current_overall_rank'].fillna(dd['current_overall_rank'].mean())
dd.head()
#median
dd['watchers'] = dd['watchers'].fillna(dd['watchers'].median())
dd.head()
dd.info()
dd.isnull().sum()
~~~

## Loan_data.csv
~~~
import numpy as np
import pandas as pd
import io
from google.colab import files
uploaded = files.upload()
de = pd.read_csv(io.BytesIO(uploaded['Loan_data.csv']))
print(de)
de.tail(10)
de.info()
de.isnull()
de.isnull().sum()
#mode
de['Gender'] = de['Gender'].fillna(de['Dependents'].mode()[0])
de['Dependents'] = de['Dependents'].fillna(de['Dependents'].mode()[0])
de['Self_Employed'] = de['Self_Employed'].fillna(de['Dependents'].mode()[0])
de.head()
#mean
de['LoanAmount'] = de['LoanAmount'].fillna(de['LoanAmount'].mean())
de['Loan_Amount_Term'] = de['Loan_Amount_Term'].fillna(de['Loan_Amount_Term'].mean())
de.tail()
#median
de['Credit_History'] = de['Credit_History'].fillna(de['Credit_History'].median())
de.head()
de.info()
de.isnull().sum()
~~~

# OUPUT
## Data_set
![1](https://user-images.githubusercontent.com/53014593/188911025-7ff03656-af23-423a-a144-64b6a3dcab95.png)
![2](https://user-images.githubusercontent.com/53014593/188911117-9e2e50a7-13c4-437d-a44e-afb42ba9aed3.png)
![3](https://user-images.githubusercontent.com/53014593/188911205-0928f901-700f-4f35-b76b-a213c9ded387.png)
![4](https://user-images.githubusercontent.com/53014593/188911309-93110a20-1069-4208-b931-1d96eaeed24b.png)
![5](https://user-images.githubusercontent.com/53014593/188911358-137b4577-b341-4759-ab71-4c1954bbeee3.png)
![6](https://user-images.githubusercontent.com/53014593/188911382-4fce6ee5-7be6-4318-988a-2a20c0d720bb.png)
![7](https://user-images.githubusercontent.com/53014593/188911413-2c531e95-e135-4d99-bf14-ad991f9cf5ac.png)
## Loan_data
![1](https://user-images.githubusercontent.com/53014593/188911528-e051c57f-93a7-454f-9ca8-6c7d6a9274a6.png)
![2](https://user-images.githubusercontent.com/53014593/188911635-32310c5b-8846-4b63-8ae0-4ee28558b7ac.png)
![3](https://user-images.githubusercontent.com/53014593/188911687-8007a153-8d45-4f65-9d43-1ddf43f60c5f.png)
![4](https://user-images.githubusercontent.com/53014593/188911721-72e33f9b-2d5c-48ba-838f-7918e8f68044.png)
![5](https://user-images.githubusercontent.com/53014593/188911756-605d2211-f238-4003-8461-b42460b7ec74.png)
![6](https://user-images.githubusercontent.com/53014593/188911784-08bc04ee-5f7b-4868-9b69-c65675a7b8cc.png)
![7](https://user-images.githubusercontent.com/53014593/188911809-3093186a-17c2-471e-9c97-1a21a2d73276.png)

# Result
The Dataset is been successfully cleaned and saved into the python file.


