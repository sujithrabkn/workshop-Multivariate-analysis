# workshop-Multivariate-analysis

# AIM:
To perform multivarient analysis on the given data set.

# ALGORITHM:
1.Clean the data

2.Remove outliers

3.Apply the skew function and Kurtosis

4.Apply Bivariate analysis on numerical and categorical

5.Apply Multivariate analysis.

# CODE

```
NAME: SUJITHRA B K N
REG NO:212222230153

## Bivariate Analysis

import pandas as pd
import numpy as py
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv('FlightInformation.csv')
df

df.head()

df.info()

df.describe()

df.isnull().sum()

df.dtypes

sns.scatterplot(df['Airline'])

sns.scatterplot(df['Route'])

sns.boxplot(x=df['Price'],y=df['Source'],data=df)

sns.barplot(x=df['Airline'],y=df['Price'],data=df)

sns.barplot(x=df['Destination'],y=df['Price'],data=df)

sns.displot(df,x="Source",hue="Route")

states=df.loc[:,["Destination","Price"]]
states=states.groupby(by=["Destination"]).sum().sort_values(by="Price")
plt.figure(figsize=(20,5))
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("DESTINATION")
plt.ylabel=("PRICE")
plt.show()

## Multivariate Analysis 

df.corr()

import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
df= pd.read_csv("FlightInformation.csv")
df= np.random.randint(low = 1, high = 100, size = (10,10))
print("The data to be plotted:\n")
print(df)
hm = sns.heatmap(data=df)
plt.show()
```
OUTPUT

RESULT
Thus the Bivariate and Multivariate analysis is observerd for the given data set.
