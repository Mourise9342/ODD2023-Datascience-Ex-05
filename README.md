# Ex:05 Feature Generation
# AIM:
To read the given data and perform Feature Generation process and save the data to a file.

# Explanation:
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

# ALGORITHM
## STEP 1
Read the given Data
## STEP 2
Clean the Data Set using Data Cleaning Process
## STEP 3
Apply Feature Generation techniques to all the feature of the data set
## STEP 4
Save the data to the file

# Program:
```
Developed by: Mourise jane
Register number: 212222230085
```
## For Encoding.csv file:
```
import pandas as pd
df=pd.read_csv('Encoding Data.csv')
df.head()
df['ord_2'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot']
en= OrdinalEncoder(categories = [climate])
df['ord_2']=en.fit_transform(df[["ord_2"]])
df
le = LabelEncoder()
df['Nom_0'] = le.fit_transform(df[["nom_0"]])
df
!pip install --upgrade category_encoders
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data = be.fit_transform(df['bin_1'])
df  = pd.concat([df,data],axis=1)
df
be = BinaryEncoder()
data = be.fit_transform(df['bin_2'])
df  = pd.concat([df,data],axis=1)
df
```
## Data.csv:
```
import pandas as pd
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
from sklearn.preprocessing import LabelEncoder,OrdinalEncoder
climate = ['Cold','Warm','Hot','Very Hot']
en= OrdinalEncoder(categories = [climate])
df1['Ord_1']=en.fit_transform(df1[["Ord_1"]])
df1
df1['Ord_2'].unique()
cl = ['High School','Diploma','Bachelors','Masters','PhD']
en= OrdinalEncoder(categories = [cl])
df1['Ord_2']=en.fit_transform(df1[["Ord_2"]])
df1
le = LabelEncoder()
df1['City'] = le.fit_transform(df1[["City"]])
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
dat = be.fit_transform(df1['bin_1'])
df1  = pd.concat([df1,dat],axis=1)
df1
from category_encoders import BinaryEncoder
be = BinaryEncoder()
data1 = be.fit_transform(df1['bin_2'])
df1  = pd.concat([df1,data1],axis=1)
df1
```
## BMI.csv file:
```
import pandas as pd
df2 = pd.read_csv("/content/bmi.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Gender'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Index'] ,columns=['Index'])
df2
```

# OUTPUT:
## For Encoding.csv
## Initial value
![1](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/5e5ce0cb-5cfa-4560-9fa4-1d49480eed22)
## Unique value:
![2](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/eedd6395-bda2-4708-a7c6-456c89a917b1)

## Ordinal encoder:
![3](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/6d630830-eb57-40b0-a7be-e11a997253bb)

## Label encoder:
![4](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/b50d7f73-a740-42c1-a901-f0611d250bef)

## Binary encoder:
![5](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/fee7efd5-8d81-43db-8387-c4e3e4dc63b8)
![6](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/2556314c-8170-4f25-b90b-4498e9c97b96)


## For Data.csv file:
## Initial data:
![1 1](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/d7fcfbdc-3fcb-4283-9aab-51133ed18c49)
## Unique data:
![1 2](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/10f469d9-8ef9-4af8-be4b-dc07d0123036)
## Ordinal encoder:
![1 3](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/8db4bcb1-a5ad-4feb-8498-f45a132961a1)
![1 5](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/908047c8-70aa-4234-823d-7e2d8f2ccb22)

## Label encoder:
![1 6](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/7b3f7f5a-b2ff-4cb2-9a11-63b587542cd7)


## Binary encoder:
![1 7](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/53109a1c-4c59-4560-a635-90100ccd6035)
![1 8](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/823d10a7-b3df-493b-a0d9-cc4a067d13f4)


## For BMI.csv file:
## Initial data:
![2 1](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/f62aa691-b8df-4406-bc3a-209007e4a306)

## Binary encoders:
![2 2](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/23e56d52-7882-4f1b-8993-0a5ac3bc39de)

## Dummies:
![2 3](https://github.com/Aakash0407/ODD2023-Datascience-Ex-05/assets/118799103/4ac1881e-8df1-4c23-9584-63e82cb01ca3)

# RESULT:
The Feature Generation process was performed and saved the data to a file.
