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
 import pandas as pd

import seaborn as sns

import matplotlib.pyplot as plt

df=pd.read_csv("titanic_dataset.csv")

df.head()

x=[1,2,3,4,5]

y=[3,6,2,7,1]

sns.lineplot(x=x,y=y)

plt.title('Line Plot')
<img width="650" height="568" alt="image" src="https://github.com/user-attachments/assets/632fd6fe-13ec-4725-8869-d94d6b5545c1" />

x=[1,2,3,4,5]

y1=[3,5,2,6,1]

y2=[1,6,4,3,8]

y3=[5,2,7,1,4]

sns.lineplot(x=x,y=y1)

sns.lineplot(x=x,y=y2)

sns.lineplot(x=x,y=y3

plt.title('Multi Line Plot')
<img width="1026" height="580" alt="image" src="https://github.com/user-attachments/assets/7c488a75-0b25-438b-a629-3956455b7dea" />

plt.figure(figsize=(8,5))

sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')

plt.title("Fare Of Passenger By Embarked Town")
<img width="1227" height="596" alt="image" src="https://github.com/user-attachments/assets/08e45446-b420-406f-b50d-811bb229284b" />

sns.scatterplot(x="Age", y="Fare", data=df)

plt.title('Scatterplot of Age vs Fare')

plt.show()
<img width="1084" height="569" alt="image" src="https://github.com/user-attachments/assets/b93993c2-92f0-4edd-a282-ff59e7648e37" />

sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))

plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')

plt.show()
<img width="1059" height="581" alt="image" src="https://github.com/user-attachments/assets/30c3fd94-eef8-4e9e-8447-bfb45f1fc8fa" />

sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
<img width="1002" height="567" alt="image" src="https://github.com/user-attachments/assets/bd681219-720c-4545-9b95-7d9541a0e203" />

sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')

plt.title("Age By Passenger Class")
<img width="968" height="566" alt="image" src="https://github.com/user-attachments/assets/a77c537e-e100-4c56-878d-8d6e5c39f770" />

sns.violinplot(x="Pclass", y="Fare", data=df)

plt.title('Violin Plot of Fare by Passenger Class')

plt.show()
<img width="1152" height="571" alt="image" src="https://github.com/user-attachments/assets/1817cbd5-f2d3-4e05-8adf-1f2132fb724b" />

sns.kdeplot(data=df['Age'], shade=True)

plt.title('Density Plot of Passenger Ages')

plt.show()
<img width="1118" height="559" alt="image" src="https://github.com/user-attachments/assets/69a54008-0290-4454-9c05-d5a8d7d62763" />

numeric_df = df.select_dtypes(include=['float64', 'int64'])

corr_matrix = numeric_df.corr()

sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')

plt.title('Heatmap of Titanic Dataset')

plt.show()
<img width="1002" height="602" alt="image" src="https://github.com/user-attachments/assets/ec4ed613-12ad-4b26-a103-bc92da365c71" />


# Result:
  the Data Visualization using seaborn python library for the given data is implemented successfully.
