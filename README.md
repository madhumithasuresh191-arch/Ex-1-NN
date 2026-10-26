## ENTER YOUR NAME: S Madhumitha
## ENTER YOUR REGISTER NO:212225040217
<H3>EX. NO.1</H3>
##DATE:26-10-2026
<H1 ALIGN =CENTER> Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
~~~
import numpy as np
import pandas as pd
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split
~~~


~~~
df=pd.read_csv('/content/Data_to_Transform.csv')
print(df)
~~~



~~~
x=df.iloc[:,:-1].values
print(x)

~~~



~~~
y=df.iloc[:,-1].values
print(y)
~~~



~~~
print(df.isnull().sum())
~~~



~~~
df.fillna(df.mean().round(1),inplace=True)
print(df.isnull().sum())
y=df.iloc[:,-1].values
print(y)
~~~



~~~
df.duplicated()
~~~



~~~
print(df['Moderate Positive Skew'].describe())
~~~


~~~
scaler=MinMaxScaler()
df1=pd.DataFrame(scaler.fit_transform(df))
print(df1)
~~~



~~~
X_train,X_test,y_train,y_test=train_test_split(x,y,test_size=0.2)
print(X_train)
print(len(X_train))
print(X_test)
print(len(X_test))
~~~










## OUTPUT:
<img width="1920" height="1020" alt="Screenshot 2026-10-26 143255" src="https://github.com/user-attachments/assets/8edddc70-31a0-4e04-aeac-00884a04e98f" />
<img width="1920" height="1020" alt="Screenshot 2026-10-26 143311" src="https://github.com/user-attachments/assets/6ecf818a-7daa-459e-833e-a6634154ffec" />
<img width="1920" height="1020" alt="Screenshot 2026-10-26 143320" src="https://github.com/user-attachments/assets/d6377ce7-5c5f-4844-bfc5-84051956c843" />
<img width="1920" height="1020" alt="Screenshot 2026-10-26 143330" src="https://github.com/user-attachments/assets/3bed32c0-2578-424e-bb94-3985eb137897" />
<img width="1920" height="1020" alt="Screenshot 2026-10-26 143339" src="https://github.com/user-attachments/assets/6b206b83-0c4d-4833-a7fc-ec6bc11bd405" />



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


