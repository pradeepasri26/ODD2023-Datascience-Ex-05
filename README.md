# Ex:05 Feature Generation
## AIM :
To read the given data and perform Feature Generation process and save the data to a file.

## EXPLANATION :
Feature Generation (also known as feature construction, feature extraction or feature engineering) is the process of transforming features into new features that better relate to the target.

## ALGORITHM :
STEP 1 : Read the given Data

STEP 2 : Clean the Data Set using Data Cleaning Process

STEP 3 : Apply Feature Generation techniques to all the feature of the data set

STEP 4 : Save the data to the file

## PROGRAM :
```
PRADEEPASRI S
212221220038
```
## bmi.csv
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
## data.csv
```
import pandas as pd
df1 = pd.read_csv("/content/data (1).csv")
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
## Encoding.csv
```
import pandas as pd
df=pd.read_csv('/content/Encoding Data (1).csv')
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
## OUTPUT:
## bmi.csv
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/bd70f391-e560-421c-947f-fc9154a01153)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/ce9f0c01-e00b-4dc6-90e5-b184521d5284)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/6e2eaba4-b854-45dc-acd7-b77411fda98a)
## data.csv
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/e19b5da1-5484-46a2-a33c-e9c683c6a597)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/d19c046c-d694-4da8-b63a-a8899840ebd4)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/757d676b-a699-4da6-921f-71f11736cc67)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/42e01be9-649a-4e3b-9f38-fc6b92bfab9c)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/80553f90-a91d-48ef-8172-df560b910623)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/283b8576-15ca-491d-adc1-4af2bbf25fa5)
## Encoding.csv
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/0f3c4b41-6d57-4604-aec0-3ccbcf146d5e)
![image](https://github.com/pradeepasri26/ODD2023-Datascience-Ex-05/assets/131433142/638be1ec-e6ac-41bc-9798-df11fe33927e)

## RESULT:
The Feature Generation process was performed and saved the data to a file.








