# Ex-04-Multivariate-Analysis
## AIM:
To perform Multivariate EDA on the given data set.

## EXPLANATION:
Exploratory data analysis is used to understand the messages within a dataset. This technique involves many iterative processes to ensure that the cleaned data is further sorted to better understand the useful meaning.The primary aim with exploratory analysis is to examine the data for distribution, outliers and anomalies to direct specific testing of your hypothesis.

## ALGORITHM:

## STEP1
Import the built libraries required to perform EDA and outlier removal.

## STEP2
Read the given csv file.

## STEP3
Convert the file into a dataframe and get information of the data.

## STEP4
Return the objects containing counts of unique values using (value_counts()).

## STEP5
Plot the counts in the form of Histogram or Bar Graph.

## STEP6
Use seaborn the bar graph comparison of data can be viewed.

## STEP7
Find the pairwise correlation of all columns in the dataframe.corr() .

## STEP8
Save the final data set into the file.

## PROGRAM:
```
Program developed by : PRAVEEN KUMAR S
Register number : 212222230108

import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt

data=pd.read_csv("SuperStore.csv")
data

data.head()

data.info()

data.describe()

data.isnull().sum()

data.dtypes

sns.scatterplot(data['Postal Code'],data['Sales'])

states=data.loc[:,["State","Sales"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES")
plt.ylabel=("SALES") 
plt.show()

states=data.loc[:,["State","Postal Code"]] 
states=states.groupby(by=["State"]).sum().sort_values(by="Postal Code") 
plt.figure(figsize=(17,7)) 
sns.barplot(x=states.index,y="Postal Code",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("STATES") 
plt.ylabel=("Postal Code") 
plt.show()

states=data.loc[:,["Segment","Sales"]] 
states=states.groupby(by=["Segment"]).sum().sort_values(by="Sales") 
plt.figure(figsize=(10,7)) 
sns.barplot(x=states.index,y="Sales",data=states) 
plt.xticks(rotation = 90) 
plt.xlabel=("SEGMENT") 
plt.ylabel=("SALES") 
plt.show()

sns.barplot(data['Postal Code'],data['Ship Mode'],hue=data['Region'])

data.corr()

sns.heatmap(data.corr(),annot=True)
```
## OUTPUT :
## DATASET
![1](https://user-images.githubusercontent.com/119559827/229698697-6774f485-fc27-486e-8804-850ba83ca859.png)

##  HEAD DATA
![2](https://user-images.githubusercontent.com/119559827/229698821-af64db5e-3683-49e2-aefb-e3ab2bbd9df6.png)

## INFORMATION
![3](https://user-images.githubusercontent.com/119559827/229698965-bb9b6949-90f5-4475-a0cc-3603cd47a7d1.png)

## DESCRIPTION
![4](https://user-images.githubusercontent.com/119559827/229699816-58f87992-a68c-4327-aa69-bfc6b8c06155.png)

## DATATYPE
![R](https://user-images.githubusercontent.com/119559827/229700277-0d4f90b7-27ed-4c57-bac6-606e9a713657.png)

## NULL DATA 
![5](https://user-images.githubusercontent.com/119559827/229700391-e7b0465d-f655-40ea-8b89-56c62a2d63c7.png)

## SCATTER PLOT
![6](https://user-images.githubusercontent.com/119559827/229700463-1a29ff9c-b652-4cd8-84cf-80187522491f.png)

## Bar plot - State and Sales
![7](https://user-images.githubusercontent.com/119559827/229700548-33ec3282-9d85-44f3-afc1-6ba252495531.png)

## Bar plot - State and Postal code
![8](https://user-images.githubusercontent.com/119559827/229700745-61ceec02-2624-4814-ac8e-04a6ac84b52d.png)

## Bar plot - Segment and Sales
![9](https://user-images.githubusercontent.com/119559827/229700907-0f01b5fd-566a-494a-92c3-bbc1119fd9f4.png)

## Bar plot - Postal code and Ship mode
![10](https://user-images.githubusercontent.com/119559827/229700966-a38c79c2-5d0a-43aa-8126-9bcf89845bfc.png)

## Correlation coefficient
![11](https://user-images.githubusercontent.com/119559827/229701049-c5de406a-8579-4f6b-adc2-9ac92a0f29f6.png)

## Heatmap
![12](https://user-images.githubusercontent.com/119559827/229701133-d9b22edf-49ef-4077-a257-63daba8861a1.png)

## RESULT:
Thus the program to perform Multivariate EDA on the given data set is successfully executed.



