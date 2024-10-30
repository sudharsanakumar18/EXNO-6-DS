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

df=sns.load_dataset("tips")
df
```
![image](https://github.com/user-attachments/assets/9c3860ab-3865-4c5f-8b72-43ee02550cbf)

```
sns.lineplot(x="total_bill",y="tip",data=df,hue='sex',linestyle='solid',legend='auto')
```
![image](https://github.com/user-attachments/assets/21088dd2-07c3-4999-9d70-4b4d107b27b0)

```
tips=sns.load_dataset('tips')
avg_total_bill=tips.groupby('day')['total_bill'].mean()
avg_tip=tips.groupby('day')['tip'].mean()
```
![image](https://github.com/user-attachments/assets/8e8585a3-f43e-44f3-9f1e-31fe5224b451)

```
plt.figure(figsize=(8,6))
p1=plt.bar(avg_total_bill.index,avg_total_bill,label='Total Bill')
p2=plt.bar(avg_tip.index,avg_tip,bottom=avg_total_bill,label='Tip')
plt.xlabel('Day')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
plt.legend()
```
![image](https://github.com/user-attachments/assets/3ff7d317-6e59-4005-a895-aba8b07adb9b)
```
import seaborn as sns
dt=sns.load_dataset('tips')
sns.barplot(x='day',y='total_bill',hue='sex',data=dt,palette='Set1')
plt.xlabel('Day of the Week')
plt.ylabel('Amount')
plt.title('Average Total Bill and Tip by Day')
```
![image](https://github.com/user-attachments/assets/a4a1628e-907b-4193-a209-0175026b3a9e)
```
tips=sns.load_dataset('tips')
sns.scatterplot(x='total_bill',y='tip',hue='sex',data=tips)
plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
```
![image](https://github.com/user-attachments/assets/af44794a-34c3-4cc3-a3a7-6503601beb09)

```
num_var = np.random.randn(1000)
num_var=pd.Series(num_var, name = "Numerical variable")
num_var
```
![image](https://github.com/user-attachments/assets/243500f8-7921-4853-94e3-769a57fac7a3)
```
sns.boxplot(x='day',y='total_bill',hue="smoker",data=tips,linewidth=2,width=0.6,boxprops={"facecolor":"red","edgecolor":"yellow"},
whiskerprops={"color":"green","linestyle":"--","linewidth":1.5},capprops={"color":"black","linestyle":"--","linewidth":1.5})
```
![image](https://github.com/user-attachments/assets/f3f60aee-a5e3-4b29-8c7c-89ecfa9fa98a)

```

import matplotlib.pyplot as plt
sns.violinplot(x="day", y="total_bill", hue="smoker", data=df, linewidth=2, width=0.6, palette="Set3", inner="quartile")
plt.xlabel("Day of the Week")
plt.ylabel("Total Bill")
plt.title("Violin Plot of Total Bill by Day and Smoker Status")
```
![image](https://github.com/user-attachments/assets/5284613b-e0ec-4b18-959c-a7ffd591ae8d)

```
import seaborn as sns
sns.set(style = 'whitegrid',palette='Set2')
tip = sns.load_dataset('tips')
sns.violinplot(x ='day', y ='tip', data = tip)

```
![image](https://github.com/user-attachments/assets/b2338e86-5efb-4025-b8ac-caba40743a4e)


```

sns.set(style = 'whitegrid')
tip = sns.load_dataset('tips')
sns.violinplot(x=tip["total_bill"])
```
![image](https://github.com/user-attachments/assets/e2888d70-ba99-45cf-8d77-5d1a70cd8a31)

```

df=sns.load_dataset("tips")
sns.kdeplot(data=df,x='total_bill',hue='time',multiple='fill',linewidth=3,palette='Set3',alpha=0.8)

```
![image](https://github.com/user-attachments/assets/dbd23436-7bcb-4d6c-9dc4-a41ab32b0ce8)

```
sns.kdeplot(data=df, x='total_bill', hue='time', multiple='stack', linewidth=3, palette='Set2', alpha=0.8)
```

![image](https://github.com/user-attachments/assets/bc917f49-7b0c-4837-934f-ff73459e61b4)
```
import numpy as np
data=np.random.randint(low=1,high=100,size=(10,10))
print("The data to be plotted")
print(data)
```
```
 hms=sns.heatmap(data=data)
```
![image](https://github.com/user-attachments/assets/abb90222-bc2b-4d09-8791-c1680b57023e)
```
hms=sns.heatmap(data=data,annot=True)
```
![image](https://github.com/user-attachments/assets/f596ecff-d38a-4d66-91eb-cff86e63e37e)
```
sns.heatmap(corr,annot=True,cmap='coolwarm')
```
![image](https://github.com/user-attachments/assets/1cdd8350-531d-4ea7-a262-3389ea5408a8)


# Result:
Thus all the data visualization techiniques of seaborn has been executed
