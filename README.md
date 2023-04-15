1.	Create A Series Using Dict In Pandas.
Ans - import pandas as pd
dic = {'a':3,'b':4,'c':7}
s=pd.Series(dic)
print(s)

2>How To Create A Copy Of The Series In Pandas?
Ans - import pandas as pd
dic = {'a':3,'b':4,'c':7}
s=pd.Series(dic)
b=s.copy()
print(b)
print(s)

3>Create a DataFrame using List
Ans - import pandas as pd
list=["radhika", "Ambika","Rushi"]
l1=pd.DataFrame(list)
l1

4>What Are The Different Ways A DataFrame Can Be Created In pandas?
Ans – 1) l1=pd.DataFrame(list)
	2) l1=pd.DataFrame(list, columns=["Name"])
	3) l1=pd.DataFrame(list, columns=["Name","Marks"])
	4) l1=pd.DataFrame(list, index=['r1','r2','r3'])

5>Write a Pandas program to join the two given dataframes along rows and assign all data
Ans - import pandas as pd
s1= {'sid': [1,2,3,4,5],
    'SName': ['Radhika','Ambika','Rushi','Pooja','Kajol'],
    'SMarks': [67, 56, 76, 89, 90]}
s2= {'sid': [6,7],
    'SName': ['Aarti','Chaitali'],
    'SMarks': [88,99]}

s3=pd.DataFrame(s1)
print("DataFrame 1")
print(s3)
s4=pd.DataFrame(s2)
print("DataFrame 2")
print(s4)
print("Concatinated DataFrame")
s=pd.concat([s3,s4])
print(s)
6>Write a Pandas program to create a Pivot table
Ans- import pandas as pd
s= pd.DataFrame({'Veggies':['Potato', 'Onion', 'Tomato', 'Onion','Potato'],
   'Amt':[45,56,32,67,43]})
pivot = s.pivot_table(index =['Veggies'], 
                       values =['Amt'], 
                       aggfunc ='sum')
print(pivot)

7>Write a Pandas program to detect missing values of a DataFrame. Display True or False
Ans - import pandas as pd
import numpy as np
list=pd.DataFrame({'StudentName':['Radhika','Ambika',np.nan,'Pooja'],
                  'StudentClass':[1,5,np.nan,np.nan]})
list.isnull()

8>Write a Pandas program to count the number of missing values in each column
Ans - import pandas as pd
import numpy as np
list=pd.DataFrame({'StudentName':['Radhika','Ambika',np.nan,'Pooja'],
                  'StudentClass':[1,5,np.nan,np.nan]})
list.isnull().sum().sum()

9>Write a Python program to find the maximum and minimum value of array
Ans - import pandas as pd
import numpy as np
list=pd.DataFrame({'StudentName':['Radhika','Ambika',np.nan,'Pooja',np.nan],
                  'StudentClass':[1,5,np.nan,np.nan,67]})
print(list.max())
print(list.min())

10>Write a NumPy program to repeat all the elements three times of a given array of string
['Pie' ,'pigeon' ,'Joker' ,'Cake']
Ans - import numpy as np
x1 = np.array(['Pie' ,'pigeon' ,'Joker' ,'Cake'])
print("Original Array:")
print(x1)
array1 = np.char.multiply(x1, 3)
print("New array:")
print(array1)




Solution :
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
titanic_df = pd.read_csv('titanic.csv')
titanic_df.head()
titanic_df.describe()
titanic_df.info()
sns.histplot(titanic_df['Age'], kde=False)
sns.scatterplot(data=titanic_df, x="Age", y="Fare", hue="Survived")
sns.boxplot(data=titanic_df, x="Survived", y="Age")
titanic_df.groupby(['Sex'])['Survived'].mean()
titanic_df.groupby(['Pclass'])['Fare'].median()
Conclusions:
- Women were more likely to survive than men.
- Passengers in first class had a higher survival rate than those in second or third class.
- The average age of passengers was around 29 years old.
