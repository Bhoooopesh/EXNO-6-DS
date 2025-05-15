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
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
sns.lineplot(x=x,y=y)
```

![image](https://github.com/user-attachments/assets/3feb1c39-dc7f-4edc-87c6-5575bac67609)

```
df = sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/64a13201-3106-4483-aae2-335c3e58b211)

```
sns.lineplot(x="total_bill",y="tip", data=df, hue="sex", linestyle='solid', legend="auto")
```



![image](https://github.com/user-attachments/assets/3bea8840-914c-4b53-912c-045ca5d49e53)

```
x=[1, 2, 3, 4, 5]
y1=[3, 5, 2, 6, 1]
y2=[1, 6, 4, 3, 8]
y3=[5, 2, 7, 1, 4]
sns.lineplot(x=x, y=y1)
sns.lineplot(x=x, y=y2)
sns.lineplot(x=x, y=y3)
plt.title("Multi-Line Plot")
plt.xlabel('X Label')
plt.ylabel("Y Label")
```

![image](https://github.com/user-attachments/assets/7d5d77e2-ca51-46cd-9579-5a9e25197a8f)


```
tips=sns.load_dataset('tips')
avg_total_bill = tips.groupby('day')['total_bill'].mean()
avg_tip = tips.groupby('day')['tip'].mean()
plt.figure(figsize=(8, 6))
p1 = plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill')
p2 = plt.bar(avg_tip.index, avg_tip, bottom=avg_total_bill, label='Tip')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```


![image](https://github.com/user-attachments/assets/88516b70-e51d-477c-8537-4fb9f3c04180)

```
avg_total_bill = tips.groupby('time')['total_bill'].mean()
avg_tip=tips.groupby('time') ['tip'].mean()
p1= plt.bar(avg_total_bill.index, avg_total_bill, label='Total Bill', width=0.4)
p2 = plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip', width=0.4)
```

![image](https://github.com/user-attachments/assets/0d1f31e9-730e-4b4a-b1ca-acede37fbace)


```
import seaborn as sns
dt= sns.load_dataset('tips')
sns.barplot(x='day', y='total_bill', hue='sex', data=dt, palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel("Total Bill")
plt.title('Total Bill by Day and Gender')
```


![image](https://github.com/user-attachments/assets/6210f3d4-9a8a-43fc-96c7-e579f6b2e1be)

```
tit=pd.read_csv("/content/titanic_dataset (1).csv")

```

![image](https://github.com/user-attachments/assets/06cbaed5-48c1-4b51-a531-113690049fc7)

```
plt.figure(figsize=(8,5))
sns.barplot(x='Embarked', y='Fare', data=tit, palette='rainbow')
plt.title("Fare of Passenger by Embarked Town")
```

![image](https://github.com/user-attachments/assets/e1ac8d5d-baa0-47eb-b4ad-81200a1494d4)

```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill', y='tip', hue='sex', data=tips)
plt.xlabel('Total Bill')
plt.ylabel("Tip Amount")
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```

![image](https://github.com/user-attachments/assets/ec5c0a1b-35d2-4f4c-bab8-9af1ee11ce7c)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```

![image](https://github.com/user-attachments/assets/35699be6-ef30-4d7a-8fac-404c2a194c2f)


```
sns.histplot(data = num_var, kde = True)
```

![image](https://github.com/user-attachments/assets/c197bed8-57d8-4800-88cb-79aa742833ec)


```
df=pd.read_csv("/content/titanic_dataset (1).csv")
sns.histplot(data=df,x="Pclass", hue="Survived", kde=True)
```

![image](https://github.com/user-attachments/assets/376f58df-66df-4bd9-89b9-bac282923626)

```
tips=sns.load_dataset('tips')
sns.boxplot(x=tips['day'], y=tips ['total_bill'], hue=tips['sex'])
```
![image](https://github.com/user-attachments/assets/58be4c6e-45ea-4582-8c24-7861350369ca)


```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```



![image](https://github.com/user-attachments/assets/93995c4b-36ef-4d7d-8415-7c3367155295)

```
sns.boxplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, boxprops={"facecolor": "lightblue", "edgecolor": "darkblue"},
whiskerprops={"color": "black", "linestyle": "--", "linewidth": 1.5}, capprops={"color": "black", "linestyle": "--", "linewidth": 1.5})
```


![image](https://github.com/user-attachments/assets/d20fac5a-ff72-4e14-b8e9-df943f3f8192)

```
sns.violinplot(x="day", y="total_bill", hue="smoker", data=tips, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```

![image](https://github.com/user-attachments/assets/f300cfbf-7565-4f5d-85f4-a84f620559fb)

```
mart=pd.read_csv("/content/titanic_dataset (1).csv")
mart
```

![image](https://github.com/user-attachments/assets/f60e4865-55d4-4a90-bac5-effd0445c8a7)

```
mart=mart[['PassengerId', 'Survived', 'Age', 'Name', 'Ticket', 'Embarked']]
mart.head(10)
```
![image](https://github.com/user-attachments/assets/6110a7f7-fa00-4483-8563-3a35e9da481d)

```
sns.kdeplot(data=mart,x='PassengerId')
```
![image](https://github.com/user-attachments/assets/07f42e17-7fdc-41ba-a7d7-de0ecd9e9168)

```
sns.kdeplot(data=mart,x='Age')
```
![image](https://github.com/user-attachments/assets/952b9538-cbe8-42d1-a759-315f595ed455)

```
sns.kdeplot(data=mart)
```

![image](https://github.com/user-attachments/assets/596bf6ba-d8db-4fc9-b00f-39634280d73a)


```
sns.kdeplot(data=mart,x='PassengerId',hue='Survived',multiple='stack')
```

![image](https://github.com/user-attachments/assets/523e6d66-bb37-42b8-8a0c-6dde4b8d92e2)

```
sns.kdeplot(data=mart,x='PassengerId',y='Survived')
```

![image](https://github.com/user-attachments/assets/dc36d49c-5f5e-4fcb-8233-bad2d1e4b470)


```
data = np.random.randint(low = 1, high = 100, size = (10,10))
hm=sns.heatmap(data=data,annot=True)
```

![image](https://github.com/user-attachments/assets/80b7d21e-c8e7-4bf1-be92-839fb818049c)



```
hm=sns.heatmap(data=data)
```

![image](https://github.com/user-attachments/assets/45c5a171-23f7-451a-bc06-61bff2b62817)







# Result:
 Include your result here
