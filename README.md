# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Collect customer data and select relevant features such as age, income, and spending score.
2. Choose the number of clusters K and initialize K cluster centroids randomly.
3. Assign each customer to the nearest centroid and recalculate the centroids based on the assigned customers.
4. Repeat the assignment and centroid calculation until the centroids no longer change, then display the customer segments.


## Program:
```
import numpy as np
from sklearn.cluster import KMeans

X = np.array([
    [18, 15],
    [20, 18],
    [22, 20],
    [25, 22],
    [40, 60],
    [42, 65],
    [45, 70],
    [48, 75],
    [70, 20],
    [75, 18],
    [80, 15],
    [85, 12]
])

kmeans = KMeans(n_clusters=3, random_state=42, n_init=10)
kmeans.fit(X)

print("Customer Segments:")
print(kmeans.labels_)

print("Cluster Centers:")
print(kmeans.cluster_centers_)

income = float(input("Enter Annual Income: "))
score = float(input("Enter Spending Score: "))

cluster = kmeans.predict([[income, score]])

print("Customer belongs to Cluster:", cluster[0])
```
Developed by: NAREN.V
RegisterNumber:  212225080035


## Output:
![K Means Clustering for Customer Segmentation](sam.png)


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
