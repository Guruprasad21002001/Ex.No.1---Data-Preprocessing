# Ex.No.1---Data-Preprocessing
##AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## REQUIPMENTS REQUIRED:
 Hardware – PCs
 Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

Kaggle :
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

Data Preprocessing:

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

Need of Data Preprocessing :

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


##ALGORITHM:
Importing the libraries
Importing the dataset
Taking care of missing data
Encoding categorical data
Normalizing the data
Splitting the data into test and train

##PROGRAM:
~~~
Register Number: 212221230032
Name: GURUPRASAD.B
import pandas as pd
df=pd.read_csv("/content/Churn_Modelling.csv")
df.head()
df.isnull().sum()
df.drop(["RowNumber","Age","Gender","Geography","Surname"],inplace=True,axis=1)
print(df)
x=df.iloc[:,:-1].values
y=df.iloc[:,-1].values
print(x)
print(y)
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
df1 = pd.DataFrame(scaler.fit_transform(df))
print(df1)
from sklearn.model_selection import train_test_split
xtrain,ytrain,xtest,ytest=train_test_split(x,y,test_size=0.2,random_state=2)
print(xtrain)
print(len(xtrain))
print(xtest)
print(len(xtest))
from sklearn.preprocessing import StandardScaler
sc = StandardScaler()
df1 = sc.fit_transform(df)
print(df1)
~~~

##OUTPUT:

## Dataset:

![OP1](https://user-images.githubusercontent.com/95342910/192080344-ea12bdd1-de16-4f92-a8bd-8e4719f2db8d.png)


## Discribing data:

![OP2](https://user-images.githubusercontent.com/95342910/192080363-44fc1b23-5c42-4c94-9bef-0e247067672a.png)

## Normalized data:

![OP3](https://user-images.githubusercontent.com/95342910/192080396-3cbecbe1-0b0b-4d54-a08c-c41fdcd402f8.png)

## X_train and Y_train values: 

![OP4](https://user-images.githubusercontent.com/95342910/192080406-36c27c26-0c0e-4cf9-91fe-cb8990be424a.png)

## X and Y values:

![OP5](https://user-images.githubusercontent.com/95342910/192080422-e20f7e19-4785-4798-98b7-aecb8e7591ee.png)

## X_test and Y_test values:

![OP6](https://user-images.githubusercontent.com/95342910/192080478-7cc7c62b-8b18-441f-820c-d61b632639a3.png)


## RESULT
Thus the above program for standardizing the given data was implemented successfully
