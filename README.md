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

## Numerical and Numerical

### Scatter plot:

sns.scatterplot(df['Airline'])

sns.scatterplot(df['Source'])

## Numerical & Categorical

### Bar Plot:

sns.barplot(x=df['Airline'],y=df['Price'],data=df)

sns.barplot(x=df['Destination'],y=df['Price'],data=df)

states=df.loc[:,["Destination","Price"]]
states=states.groupby(by=["Destination"]).sum().sort_values(by="Price")
plt.figure(figsize=(20,5))
sns.barplot(x=states.index,y="Price",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("DESTINATION")
plt.ylabel=("PRICE")
plt.show()

### Box Plot:

sns.boxplot(x=df['Price'],y=df['Source'],data=df)

sns.boxplot(x=df['Price'],y=df['Duration'],data=df)

### Dist Plot:

sns.displot(df,x="Source",hue="Route")

sns.displot(df,x="Airline",hue="Destination")

## Multiveriate

df.corr()

sns.heatmap(df.corr(),annot=True)
```
# OUTPUT:

## DATA SET:

![Screenshot 2023-04-05 200535](https://user-images.githubusercontent.com/119477857/230124841-bf8e54ab-64b2-45c0-8d21-0c865a64ea40.png)

## INFO:

![Screenshot 2023-04-05 200546](https://user-images.githubusercontent.com/119477857/230126525-60c90a49-6d0d-4d55-86fa-c82a91428f1b.png)

## DESBRIBE:

![Screenshot 2023-04-05 200623](https://user-images.githubusercontent.com/119477857/230128017-da8ca1cb-7d44-476c-a88d-c98d33288741.png)

## SUM:

![Screenshot 2023-04-05 200911](https://user-images.githubusercontent.com/119477857/230129262-ae419190-7587-494d-8d9a-6efbcdba9f97.png)

## DTYPES:

![Screenshot 2023-04-05 200956](https://user-images.githubusercontent.com/119477857/230129496-14d4656c-282a-4b87-b066-5519c0adf59d.png)

## Numerical and Numerical

### Scatter plot:

![Screenshot 2023-04-05 201020](https://user-images.githubusercontent.com/119477857/230130474-bef98d4b-8adf-4e4c-bc4f-1dfe236a7a44.png)

![Screenshot 2023-04-05 201055](https://user-images.githubusercontent.com/119477857/230130508-321963c7-e4b7-4423-aa0e-c0bd4cd00fd1.png)

## Numerical & Categorical

### Bar Plot:

![Screenshot 2023-04-05 201236](https://user-images.githubusercontent.com/119477857/230130905-841be414-b7d9-4503-8a61-bb0662af5f0d.png)

![Screenshot 2023-04-05 201450](https://user-images.githubusercontent.com/119477857/230130969-d21a4c6c-a029-4bc8-bbb9-d9988077e3cb.png)

![Screenshot 2023-04-05 201511](https://user-images.githubusercontent.com/119477857/230131031-a3113935-41d7-4f05-ba1a-418ed92f9d63.png)

### Box Plot:

![Screenshot 2023-04-05 210616](https://user-images.githubusercontent.com/119477857/230131448-cb987271-f3ca-4ab4-b4cd-0ff1008fe03b.png)

![Screenshot 2023-04-05 201530](https://user-images.githubusercontent.com/119477857/230131141-e5a344a8-a4e4-4f86-a615-b5f4dc75ecfa.png)

### Dist Plot:

![Screenshot 2023-04-05 201726](https://user-images.githubusercontent.com/119477857/230131833-0812a627-4ee3-49b8-91b2-5f80513c296a.png)

![Screenshot 2023-04-05 201809](https://user-images.githubusercontent.com/119477857/230131876-94f0fc89-1268-41cf-ad87-8cfe8427975e.png)

## MULTIVERIATE:

![Screenshot 2023-04-05 211522](https://user-images.githubusercontent.com/119477857/230135043-3617f860-8545-4fcb-8ec3-12c8ba3f6312.png)

![Screenshot 2023-04-05 211537](https://user-images.githubusercontent.com/119477857/230135105-c1bc0065-06a9-46f5-9f2b-8d243c44aab1.png)

# RESULT
Thus the Bivariate and Multivariate analysis is observerd for the given data set.
