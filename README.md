# EXNO2DS
# AIM:
      To perform Exploratory Data Analysis on the given data set.
      
# EXPLANATION:
  The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.
  
# ALGORITHM:
STEP 1: Import the required packages to perform Data Cleansing,Removing Outliers and Exploratory Data Analysis.

STEP 2: Replace the null value using any one of the method from mode,median and mean based on the dataset available.

STEP 3: Use boxplot method to analyze the outliers of the given dataset.

STEP 4: Remove the outliers using Inter Quantile Range method.

STEP 5: Use Countplot method to analyze in a graphical method for categorical data.

STEP 6: Use displot method to represent the univariate distribution of data.

STEP 7: Use cross tabulation method to quantitatively analyze the relationship between multiple variables.

STEP 8: Use heatmap method of representation to show relationships between two variables, one plotted on each axis.

## CODING AND OUTPUT

``
import pandas as pd

import numpy as np

import seaborn as sns

df=pd.read_csv('/content/titanic_dataset.csv')

df

``
<img width="1401" height="613" alt="image" src="https://github.com/user-attachments/assets/319a1452-e415-4069-a410-acfbc4f7245b" />

``
df.info()
``


<img width="724" height="422" alt="image" src="https://github.com/user-attachments/assets/457eb553-3c42-439c-9f03-1e0b553b6a5f" />

``
df.describe()
``


<img width="1113" height="373" alt="image" src="https://github.com/user-attachments/assets/cec963df-7902-41e1-826e-f12ea76c2f2d" />

``
df.dtypes
``

<img width="408" height="572" alt="image" src="https://github.com/user-attachments/assets/dea83aa1-ded0-439b-bd85-9d777ed4c52b" />

``
df.shape
``

<img width="180" height="41" alt="image" src="https://github.com/user-attachments/assets/012dda74-fba8-4a83-99a3-0cf0e6fa810a" />

``
df.value_counts()
``

<img width="1389" height="700" alt="image" src="https://github.com/user-attachments/assets/2cb30531-897e-46d2-b12f-98ef3d5f791f" />

``
df['Age'].value_counts()
``

<img width="290" height="603" alt="image" src="https://github.com/user-attachments/assets/7adb6be5-ddf9-4e7d-99e9-750faf0f4589" />

``
df.set_index('PassengerId',inplace=True)
df
``

<img width="1356" height="633" alt="image" src="https://github.com/user-attachments/assets/1b64f1a0-cead-46ba-96d1-b9b0614ae9d1" />

``
df.nunique()
``

<img width="319" height="525" alt="image" src="https://github.com/user-attachments/assets/af81b1b4-9d17-49f3-aa62-01c429b22a7d" />

``
sns.countplot(data=df,x='Age')
``

<img width="851" height="577" alt="image" src="https://github.com/user-attachments/assets/a7089f9a-7c0c-4213-a6fd-23f956ce9ddf" />

``
df.rename(columns={'Sex':'Gender'},inplace=True)
df
``

<img width="1363" height="643" alt="image" src="https://github.com/user-attachments/assets/580dacc8-be12-4413-9348-02ed0a71ec26" />

``
sns.catplot(x='Gender',col='Survived',kind='count',data=df,height=6,aspect=1)
``

<img width="1396" height="690" alt="image" src="https://github.com/user-attachments/assets/69a48f62-30a6-4345-bb54-967167e59570" />

``
df.boxplot(column='Age',by='Survived')
``

<img width="813" height="617" alt="image" src="https://github.com/user-attachments/assets/825c2c78-d771-4af6-ae7f-55f2f9d1f42c" />

``
sns.scatterplot(x=df['Age'],y=df['Fare'])
``

<img width="807" height="577" alt="image" src="https://github.com/user-attachments/assets/737dda5a-e3ee-4112-8dd9-6d3ec3dc8af4" />

``
plt=sns.boxplot(x='Pclass',y='Age',hue='Gender',data=df)
``

<img width="807" height="553" alt="image" src="https://github.com/user-attachments/assets/9ae8dba3-9cab-4775-8195-352ad88ac4c8" />

``
corr=df.corr(numeric_only=True)
sns.heatmap(corr,annot=True)
``

<img width="770" height="557" alt="image" src="https://github.com/user-attachments/assets/d18a22b2-f680-4156-a69d-0e136a31480c" />


# RESULT

Exploratory Data Analysis on the given data set is successful.
        
