# EX-05-Feature-Generation


## AIM
To read the given data and perform Feature Generation process and save the data to a file. 

# Explanation
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.
 

# ALGORITHM
### STEP 1
Read the given Data
### STEP 2
Clean the Data Set using Data Cleaning Process
### STEP 3
Apply Feature Generation techniques to all the feature of the data set
### STEP 4
Save the data to the file


# CODE
```
Devloped by: SANDHIYA R
Register No.: 212222230129
```
Encoding Data.csv
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
data.csv
```
df1 = pd.read_csv("data.csv")
df1.head()
df1['Ord_1'].unique()
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
titanic_dataset.csv
```
df2 = pd.read_csv("titanic_dataset.csv")
df2.head()
be = BinaryEncoder()
data2 = be.fit_transform(df2['Sex'])
df2  = pd.concat([df2,data2],axis=1)
df2
df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])
df2
```

# OUPUT
### Encoding Data.csv


### df.head()
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/2767ec3a-48f1-488f-a16e-e2041bc08d9a)

### ordinal encoder()
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/bb0737a5-5390-448f-b30a-96c90f250d9b)

### lable encoder
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/8fcf78ce-6330-44ae-9de2-10be5876d93b)
### binary encoder 
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/e8e95dd2-978c-4fdd-bb57-7b2ea4625c31)
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/7ee1ffce-a2a3-42cd-a01e-fe962e2b37a2)
### data.csv
### df.head()
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/d90663af-3ccd-49f1-95df-bb0256455431)
### ordinal encoder
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/038d9138-7f8d-4591-90bf-45a8f6c7a333)

![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/e3284bea-3dee-420e-8c53-50d36e89e58c)

#### lable encoder
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/7e798a71-6579-4f92-b43b-7dadf88264ad)
### binary encoder
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/7c16d964-690f-48a6-a749-f41170d7a363)
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/d8f85547-bcc7-4e4c-949c-5351e4185f22)

### titanic_dataset.csv
### df.head()
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/702d6251-c5d2-436f-8d6c-afc18838f2c6)
### binary encoder
![image](https://github.com/SandhiyaR1/EX-05-Feature-Generation/assets/113497571/cf078656-6d5c-49cd-9c91-762c31c421c9)
# RESULT
The Feature Generation process was performed and saved the data to a file.
