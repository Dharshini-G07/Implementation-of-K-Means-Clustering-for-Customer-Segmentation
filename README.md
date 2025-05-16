# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Start the program and import necessary libraries.

2.Load the CSV file using pandas.

3.Display basic information and check for null values.

4.Import KMeans from sklearn.

5.Create an empty list to store WCSS values.

6.Run a loop from 1 to 10 and apply KMeans clustering.

7.Store WCSS (inertia) values in the list.

8.Plot the Elbow graph to find the best number of clusters.



## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: PRIYADHARSHINI G
RegisterNumber:  212224230209
*/
```
```
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range(1,11):
    kmeans=KMeans(n_clusters=i,init="k-means++")
    kmeans.fit(data.iloc[:,3:])
    wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss)
plt.xlabel("No. of. clusters")
plt.ylabel("wcss")
plt.title("Elbow method")
print("Name: Priyadharshini G")
print("Reg no : 212224230209")
```

## Output:

## data.head()
![image](https://github.com/user-attachments/assets/9dcc89c6-65fd-4728-9000-137163c0bfc9)

## data.info()
![image](https://github.com/user-attachments/assets/93ca24d1-add1-4c84-8642-ccea061bb707)

## data.isnull().sum()
![image](https://github.com/user-attachments/assets/d876991d-4133-480a-aacf-0d5c9b437496)

## graph
![image](https://github.com/user-attachments/assets/fd53c519-f4c8-4626-a289-a9a6841a6838)



## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
