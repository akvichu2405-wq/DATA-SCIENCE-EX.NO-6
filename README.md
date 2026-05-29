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
 NAME:VISHNU PRIYA A K
 REF:
 212225230309


```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```

<img width="1187" height="191" alt="image" src="https://github.com/user-attachments/assets/bdc57466-bbda-473b-9c2f-f6e7ce509ee7" />


```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```

<img width="663" height="538" alt="image" src="https://github.com/user-attachments/assets/ed0cfd74-8e3f-4a7e-9bcf-d52b1b2d0e22" />

```
x=[1,2,3,4,5]
y1=[3,5,2,6,1]
y2=[1,6,4,3,8]
y3=[5,2,7,1,4]
sns.lineplot(x=x,y=y1)
sns.lineplot(x=x,y=y2)
sns.lineplot(x=x,y=y3)
plt.title('Multi Line Plot')
```

<img width="668" height="534" alt="image" src="https://github.com/user-attachments/assets/b3d0b534-3154-45f2-a754-836072f2f74d" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="869" height="582" alt="image" src="https://github.com/user-attachments/assets/8eb2c616-f33e-4ccb-8285-b3b38c1a908b" />


```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```

<img width="726" height="554" alt="image" src="https://github.com/user-attachments/assets/7b5600f4-d18b-4999-882f-8d0c54b46dc0" />


```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```

<img width="710" height="568" alt="image" src="https://github.com/user-attachments/assets/9cbcdc0e-2080-4a88-b118-33ed58af96a1" />


```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```

<img width="705" height="538" alt="image" src="https://github.com/user-attachments/assets/98efdb2c-1b8c-49d5-b607-5ab98f478ff9" />


```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```

<img width="699" height="554" alt="image" src="https://github.com/user-attachments/assets/ac4a2ada-62dd-4361-b9d2-3229a2cf8cb5" />


```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```

<img width="712" height="563" alt="image" src="https://github.com/user-attachments/assets/06d0f357-9f62-4587-a44c-f91160d9f8e8" />


```
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```

<img width="729" height="554" alt="image" src="https://github.com/user-attachments/assets/b6356052-546d-4643-b1af-76f77d75f1f0" />


```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```

<img width="748" height="627" alt="image" src="https://github.com/user-attachments/assets/57aab11b-f0e1-4e1a-ac45-fd44fdccce31" />

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
