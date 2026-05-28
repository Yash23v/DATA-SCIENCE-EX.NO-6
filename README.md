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
```
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
df=pd.read_csv("titanic_dataset.csv")
df.head()
```
<img width="1187" height="191" alt="image" src="https://github.com/user-attachments/assets/ecf06243-bbc6-4d6e-a6bc-864fa59b0773" />

```
x=[1,2,3,4,5]
y=[3,6,2,7,1]
sns.lineplot(x=x,y=y)
plt.title('Line Plot')
```
<img width="663" height="538" alt="image" src="https://github.com/user-attachments/assets/fed27226-ae47-450a-a6c4-37648e75f85a" />

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
<img width="668" height="534" alt="image" src="https://github.com/user-attachments/assets/080daf47-6dc3-40db-a6ce-cada97e0123c" />

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked',y='Fare',data=df,palette='rainbow')
plt.title("Fare Of Passenger By Embarked Town")
```
<img width="869" height="582" alt="image" src="https://github.com/user-attachments/assets/f3050da5-3919-4ebd-be59-13815bad76b9" />

```
sns.scatterplot(x="Age", y="Fare", data=df)
plt.title('Scatterplot of Age vs Fare')
plt.show()
```
<img width="726" height="554" alt="image" src="https://github.com/user-attachments/assets/5cda92ff-491e-4a45-b7f4-6ef963e31d84" />

```
sns.scatterplot(x="Age", y="Fare", size="Pclass", data=df, sizes=(30, 200))
plt.title('Bubble Chart of Age vs Fare, Size by Passenger Class')
plt.show()
```
<img width="710" height="568" alt="image" src="https://github.com/user-attachments/assets/3c059bb2-36bf-41db-afb4-7b67ce155ca5" />

```
sns.histplot(data=df,x="Pclass",hue="Survived",kde=True)
```
<img width="705" height="538" alt="image" src="https://github.com/user-attachments/assets/9e57e420-ed6c-4126-9676-3f89a71c0f15" />

```
sns.boxplot(x='Pclass',y='Age',data=df,palette='rainbow')
plt.title("Age By Passenger Class")
```
<img width="699" height="554" alt="image" src="https://github.com/user-attachments/assets/05733dff-44ea-40e4-88b4-197d1c39f546" />

```
sns.violinplot(x="Pclass", y="Fare", data=df)
plt.title('Violin Plot of Fare by Passenger Class')
plt.show()
```
<img width="712" height="563" alt="image" src="https://github.com/user-attachments/assets/9bb9b8eb-e071-4800-b3c6-5e4f26ed23cc" />

```
sns.kdeplot(data=df['Age'], fill=True)
plt.title('Density Plot of Passenger Ages')
plt.show()
```
<img width="729" height="554" alt="image" src="https://github.com/user-attachments/assets/9ba0f40d-c9ab-458e-a34a-6015f6e07a1d" />

```
numeric_df = df.select_dtypes(include=['float64', 'int64'])
corr_matrix = numeric_df.corr()
sns.heatmap(corr_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Titanic Dataset')
plt.show()
```
<img width="748" height="627" alt="image" src="https://github.com/user-attachments/assets/a94162ec-cc81-41fb-a866-6e73061074d1" />

# Result:
Thus, all the data visualization techniques of seaborn has been implemented.
