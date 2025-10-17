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
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
x = [1, 2, 3, 4, 5]
y = [3, 6, 2, 7, 1]
plt.figure(figsize=(8, 5))
sns.lineplot(x=x, y=y)
plt.title('Simple Line Plot using Seaborn')
plt.xlabel('X-Values')
plt.ylabel('Y-Values')
plt.grid(True)
plt.show()

<img width="833" height="529" alt="image" src="https://github.com/user-attachments/assets/bc49ea77-6a76-4e55-8637-ebd50116b779" />

x = [1, 2, 3, 4, 5]
y1 = [3, 5, 2, 6, 1]
y2 = [1, 6, 4, 3, 8]
y3 = [5, 2, 7, 1, 4]
data = pd.DataFrame({'X': x, 'Y1': y1, 'Y2': y2, 'Y3': y3})
data_long = data.melt('X', var_name='Series', value_name='Y_Value')

plt.figure(figsize=(8, 5))
sns.lineplot(data=data_long, x='X', y='Y_Value', hue='Series', style='Series', markers=True, dashes=False)
plt.title('Multiple Line Plots using Seaborn')
plt.xlabel('X-Value')
plt.ylabel('Y-Value')
plt.legend(title='Data Series')
plt.grid(True)
plt.show()

<img width="856" height="531" alt="image" src="https://github.com/user-attachments/assets/2635b8d9-6c11-460a-bcd9-d99d8d4f2aa3" />

tips = sns.load_dataset('tips')
plt.figure(figsize=(8, 5))
sns.barplot(x='day', y='total_bill', hue='sex', data=tips, palette='viridis')

plt.xlabel('Day of the Week')
plt.ylabel('Total Bill (Average)')
plt.title('Average Total Bill by Day and Gender')
plt.show()

<img width="858" height="538" alt="image" src="https://github.com/user-attachments/assets/b538afad-0f9b-4e84-b130-9453cd01b2fe" />

tit = sns.load_dataset('titanic')
tit.head()

<img width="958" height="203" alt="image" src="https://github.com/user-attachments/assets/587d15ae-a9cd-41e1-ae85-9fec31d48d62" />

plt.figure(figsize=(8,5))
sns.barplot(x='embark_town', y='fare', data=tit, palette='rainbow', errorbar=None)
plt.title('Fare of Passenger by Embarked Town')
plt.xlabel('Embarked Town')
plt.ylabel('Fare (Average)')
plt.show()

<img width="827" height="533" alt="image" src="https://github.com/user-attachments/assets/a581e0e8-2648-485e-826e-dd0553713cdf" />

plt.figure(figsize=(8,5))
sns.barplot(x='embark_town', y='fare', data=tit, palette='rainbow', hue='pclass', errorbar=None)
plt.title('Fare of Passenger by Embarked Town, Divided by Class')
plt.xlabel('Embarked Town')
plt.ylabel('Fare (Average)')
plt.legend(title='Passenger Class')
plt.show()

<img width="859" height="541" alt="image" src="https://github.com/user-attachments/assets/00fdf626-d241-41c0-b9b5-70f550b1bdcc" />

import seaborn as sns
plt.figure(figsize=(8, 5))
sns.scatterplot(x='total_bill', y='tip', data=tips, hue='time', style='smoker')

plt.xlabel('Total Bill')
plt.ylabel('Tip Amount')
plt.title('Scatter Plot of Total Bill vs. Tip Amount')
plt.show()

<img width="896" height="547" alt="image" src="https://github.com/user-attachments/assets/2631c1ff-ca03-4985-b507-00cf84364f4f" />

plt.figure(figsize=(8, 5))
sns.violinplot(x='pclass', y='age', data=tit, hue='sex', split=True, palette='Pastel1')
plt.title('Age Distribution by Passenger Class and Sex (Violin Plot)')
plt.xlabel('Passenger Class')
plt.ylabel('Age')
plt.legend(title='Sex')
plt.show()

<img width="525" height="248" alt="image" src="https://github.com/user-attachments/assets/722e5dcb-bd55-40ab-9076-000ccc1f6dfb" />

import seaborn as sns
import numpy as np
import pandas as pd
np.random.seed(0)
marks = np.random.normal(loc=70, scale=10, size=100)
np.random.seed(1)
num_var = np.random.randn(1000)
num_var = pd.Series(num_var, name = "Numerical Variable")
num_var

<img width="882" height="533" alt="image" src="https://github.com/user-attachments/assets/ef947e6b-6b9a-469b-9272-7f50193586d4" />

plt.figure(figsize=(8, 5))
sns.histplot(num_var, kde=True, bins=30, color='skyblue')
plt.title('Histogram of Numerical Variable with KDE')
plt.xlabel('Numerical Variable')
plt.ylabel('Frequency')
plt.show()

<img width="846" height="531" alt="image" src="https://github.com/user-attachments/assets/f156c820-67aa-4460-b9ab-069923d9132b" />

plt.figure(figsize=(8, 5))
sns.histplot(data=tit, x='pclass', hue='survived', kde=False, multiple='stack', palette='tab10')
plt.title('Passenger Class Distribution by Survival (Stacked Histogram)')
plt.xlabel('Passenger Class (1, 2, 3)')
plt.ylabel('Count')
plt.legend(title='Survived', labels=['Yes', 'No'])
plt.xticks(ticks=[1, 2, 3])
plt.show()

<img width="892" height="536" alt="image" src="https://github.com/user-attachments/assets/3cf24f37-6612-4eee-99cb-0cf8869a74b3" />

# Result:
 
Thus the program to Perform Data Visualization using seaborn python library for the given datas is executed successfully.
