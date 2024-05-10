# EXNO-6-DS-DATA VISUALIZATION USING SEABORN LIBRARY

# Aim:
  To Perform Data Visualization using seaborn python library for the given datas.

# EXPLANATION:
Data visualization is the graphical representation of information and data. By using visual elements like charts, graphs, and maps, data visualization tools provide an accessible way to see and understand trends, outliers, and patterns in data.

# Algorithm:
STEP 1:Include the necessary Library.

STEP 2:Read the given Data.

STEP 3:Apply data visualization techniques to identify the patterns of the data.

STEP 4:Apply the various data visualization tools wherever necessary.

STEP 5:Include Necessary parameters in each functions.

# Coding and Output:
 ```python
import pandas as pd
df=pd.read_csv("/content/titanic_dataset.csv")
df.head()
import seaborn as sns
import matplotlib.pyplot as plt
```
## 1. LinePlot
   ```python
   x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/20601ff6-8f56-4839-a243-82790914cdc0)


## 2. Multiline Plot
```python
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/2f3b27d3-1621-4845-acb8-2f038d59ede9)


## Too visualize Relationships
## 1. Barchart
```python
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/b895688a-e0c9-48e3-a247-17f9c6a8adf6)



## 2. Scatter Plot
```python
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/dc977f22-e660-4448-85d0-d60ad8921e10)

## 3.Bubble Chart
```python
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/b81b27d2-fea5-47bd-bea6-e5c6470e2838)

## To capture distributions
## 1.Histogram
```python
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/0e593cf8-49dd-4a2c-b786-90aecbc7a15f)

## 2.Box Plot
```python
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/e3609384-0a78-4e12-a34c-b6302c7e6ce7)

## 3. Violin plot
```python
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/03737ad1-14b0-495b-a90d-c91bef7974a5)

## 4. Density plot
```python
sns.kdeplot(data=df['Age'], shade=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/9b504dd8-05ef-45b0-9512-4788cf787507)

## 5. Heat map
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
![image](https://github.com/svarsha220/EXNO-6-DS/assets/127709117/1da40f88-8bd7-448d-a70d-6fbde85040b2)

# Result:
 Thus, the Data Visualization using seaborn python library for the given data is implemented successfully.
