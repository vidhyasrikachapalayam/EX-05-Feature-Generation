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
import pandas as pd

df=pd.read_csv('/content/Encoding Data.csv')

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

df1 = pd.read_csv("/content/data.csv")

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

df2 = pd.read_csv("/content/titanic_dataset.csv")

df2.head()

be = BinaryEncoder()

data2 = be.fit_transform(df2['Sex'])

df2  = pd.concat([df2,data2],axis=1)

df2

df2 = pd.get_dummies(df2, prefix=['Embarked'] ,columns=['Embarked'])

df2






# OUPUT

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/6816e4a4-6836-4fc9-a21f-33676e1c8333)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/40b65ea2-8ab7-4d93-88e0-2070bc57ee25)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/a059f816-5f57-4269-82f8-4119dee71d20)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/73088259-75fb-4d35-bbaf-9578763949db)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/899d4569-b326-45ee-b1f4-88422b75ad0f)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/b339e6b2-6e79-41fa-bac8-97d4bd031b0e)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/8b9c75cb-5016-4133-a628-c862bc3ff528)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/9b6f025e-45d2-49c5-b293-6c532c62b78e)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/d824f714-901f-48ee-86b2-ddb04975e8ab)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/bc71717d-7071-448f-98e3-c899de90da1e)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/87b16bd2-6095-456e-83c3-016cd0b7a17b)

![image](https://github.com/vidhyasrikachapalayam/EX-05-Feature-Generation/assets/119477817/85f4bf63-6b18-4417-99a3-b0d9077e2683)


RESULT

The Feature Generation process was performed and saved the data to a file.

