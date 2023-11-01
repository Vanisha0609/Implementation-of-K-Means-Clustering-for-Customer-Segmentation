# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the necessary packages using import statement.
2. Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().
3. Import KMeans and use for loop to cluster the data.
4. Predict the cluster and plot data graphs.
5. Print the outputs and end the program

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: Vanisha Ramesh
RegisterNumber: 212222040174

import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv('/content/Mall_Customers.csv')

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
wcss=[]

for i in range (1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)

plt.plot(range(1,11),wcss,color="cadetblue")
plt.xlabel("No. of Clusters")
plt.ylabel("wcss")
plt.title("Elbow Method")

km=KMeans(n_clusters = 5)
km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])
y_pred

data["cluster"]=y_pred
df0 = data[data["cluster"]==0]
df1 = data[data["cluster"]==1]
df2 = data[data["cluster"]==2]
df3 = data[data["cluster"]==3]
df4 = data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="mediumpurple",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="darkseagreen",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="lightskyblue",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="pink",label="cluster4")
plt.legend()
plt.title("Customer Segments")
*/
```


## Output:
1.data.head()

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/ba70ff30-fb60-413b-847f-e7d2b9be2634)

2.data.info():

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/1279ffdb-e374-4c80-95ad-4b4c35cad1f8)

3.null value:

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/cb138022-04ef-488c-8f04-c33d36be54f1)

4.Elbow Graph:

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/4718670e-6fc4-4ec9-93cd-74452f0c361a)

5.Cluster Formation:

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/92b2da18-dcef-427b-bed4-6ee8d8c7ed64)

6.predicted value:

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/314b45b6-8d9b-4cf1-aae1-d8cba5d19cfd)

7.Cluster representing customer-segments graph:

![image](https://github.com/Vanisha0609/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/119104009/05a89f92-79e5-4f82-a7f7-f984a60e923b)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
