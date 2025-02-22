# Implementation of K-Means Clustering Algorithm

## Aim
To write a python program to implement K-Means Clustering Algorithm.

## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1:
Load the CSV into a DataFrame.
<br>

### Step2:
Print the number of contents to be displayed using df.head().
<br>

### Step3:
The number of rows returned is defined in pandas option settings.
<br>

### Step4:
Check your system's maximum column with the pd.options.display.max_column statement.
<br>

### Step5:
Increase the maximum number of rows to display the entire DataFrame.
<br>

## Program:
##Developed by : A.Ruchitha Reddy

##Reg.no : 21005032

```python

import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')

X1 = pd.read_csv('clustering.csv')
print(X1.head(2))
X2 = X1.loc[:, ['ApplicantIncome', 'LoanAmount']]
print(X2.head(2))

X = X2.values
sns.scatterplot(X[:,0], X[:, 1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

kmean=KMeans(n_clusters=4)
kmean.fit(X)

print('Cluster Centers:', kmean.cluster_centers_)
print('Labels:', kmean.labels_)

predicted_class = kmean.predict([[9000,120]])
print('The cluster group 1for Applicant Income 9000 and Loanamount 120')

```
## Output:
![output](https://github.com/RuchithaReddy28/K-Means-Clustering-algorithm/blob/master/x1.PNG?raw=true)
![output](https://github.com/RuchithaReddy28/K-Means-Clustering-algorithm/blob/master/x2.PNG?raw=true)
<br>

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.