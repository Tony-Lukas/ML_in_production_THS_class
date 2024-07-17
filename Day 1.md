
# Day 1: Python and Tools

---
# Todo
 [Abody.ai](https://www.abody.ai/)
သူတို့ဘယ်လို ညွှန်းလဲဆိုတာတွေကို စမ်းကြည့်ကြည့်ပါ။

---
# Python
+ [Python.org](https://www.python.org/) မှာ python ကို down ပါ။
+ သုံးတဲ့အခါ version 2 ခုလောက်ခွာသုံးပါ။ 
+ python က update ခဏခဏထွက်ပေမယ့် တခြားကောင်က  update ခဏခဏမထွက်ဘူး။ 
+ current 3.12 $\Rightarrow$ use 3.10

---
# To run 
1. Local Machine
2. [Colab](https://colab.research.google.com/) & [Kaggle](https://www.kaggle.com/)

[Colab vs Kaggle: Which is better](https://www.kaggle.com/discussions/product-feedback/147587)
---
# GPU
1. [Colab](https://colab.research.google.com/)
2.  [Kaggle](https://www.kaggle.com/)
3. [Paperspace](https://www.paperspace.com/)  
Paperspace ကသာမာန် run တာလောက် free ရနိုင်။

---
# Virtual Environment
- [Anaconda](https://www.anaconda.com/)
- [pipenv](https://pipenv.pypa.io/en/latest/)
- [venv](https://docs.python.org/3/library/venv.html)

---
# Why Anaconda
- စက်တလုံးမျာ python version နှစ်မျိုးသုံးမျိုးသုံးချင်လို့

---
# Useful conda comment
- `conda env list` $\Rightarrow$ ==show list of env in your machie==
- `conda create -n env_name python_version`$\Rightarrow$ ==to create new env==
- `conda acivate env_name` $\Rightarrow$ ==to activate env==

---
# Why we need to know Git
To versioning
- infer structure (server)
- model
- data
- experiment (experiment tracking)

---
# Git comment 
- `git clone https://github.com/tharhtetsan/ML-in-Prod-batch-1.git`
- `git add .`
- `git commit -m "massage"`
- `git puch`
- `git status`

---
# IDE
- [virtual studio code](https://code.visualstudio.com/)

---
# Todo in vscode
Cttl+p`=> shall Command: Install 'code' command in PATH

---
# Why VS code
- Rich Extension
	- python
	- jupyter
	
---
# README.md
- [markdown](https://www.markdownguide.org/) နဲ့ရေးထားတယ်။ ရေးတတ်အောင်အကျင့်လုပ်စေချင်တယ်။
- Documentation ရေးဖို့အတွက်သုံးပါတယ်

---
# To install
1. [Python.org](https://www.python.org/)
2.  [Anaconda](https://www.anaconda.com/)
3. [GitHub Desktop](https://github.com/apps/desktop) & [Fork](https://git-fork.com/)
4. [vscode](https://code.visualstudio.com/)

---
# python tip
1. data type မသိရင် ==`type(var_name)`== ဆိုပြီးစစ်လို့ရမယ်။
2. function တစ်ခုမသိရင် ==`help(func_name)`== ဆိုပြီး စစ်လို့ရတယ်။

---
# Basic data type
| Data type | Example            |
| --------- | ------------------ |
| int       | -1,0,1,456         |
| float     | 0.1, 3.14          |
| str       | "Hello World", 'A' |

---
# Basic Data structure
| Data structure Name | Example                  | syntax        |
| ------------------- | ------------------------ | ------------- |
| List                | `[1,'a',0.1]`            | `[]`          |
| Set                 | {1,2,3}                  | `{}`          |
| Tuple               | (1,2,3)                  | `()`          |
| Dictionary          | {"name":"MgMg","age":12} | `{key:value}` |

```python
range(start, end, step)
None
```

---
# Comment
+ ==#== $\Rightarrow$ comment
+ =="""==  $\Rightarrow$ documenting

---

# For Looping

```python
# for each
for item in list_name:
	print(item)
```

```python
# for loop
for index in rane(len(list_name)):
	print(list_name[index])
```

---
# While Loop
```python
# while
i = 0 # init
while i<10: #condition
	print(i)
	i += 1 # increase
```

```python
#Do while
i=1 
while True:
	print(i)
	i +=1
	if i<10:
		break # to exit the loop
```

---
# Function

- to define function use ==def== keyword
```python
def addTwoNumber(num1, num2):
	return num1+num2
```

---
# Best practice
```python
def addTwoNumber(num1:int,num2 = 0)->int:
	"""
	add two number and return result
	"""
	return a+b
```
- Give the ==meaningful== function name
- Use type hinting and return type
- Use default value
---
# Pass by value vs Pass by Reference
```python

a = [3,4,2,1]
#pass by reference
b = a
a[0] = 5
print(a,b)

#pass by value
c = a.copy()
a[1]=6
print(a,c)
```

---
## Example 2
```python
a = [3,4,2,1]
# a.sort() function change value of 'a' and no return value
print(a.sort())
print(a)

c = [3,4,2,1]
# sorted() function take value of 'c' array and return sorted array, but no change 'c'
print(sorted(c))
print(c)
```

---
# Class
```python
class Person:
	# Constructor
	def __init__(self,name,age=0) ->None:
		self.name =name
		self.age = age
```

Object ကိုယ်တိုင်ကပိုင်ဆိုင်တာဆိုရင် ==self.var_name== ဆိုပြီးခေါ်သုံးပါတယ်။

---
# Best practice
```python
mgmg = Person(age=20,name='Mg Mg')
```
argument name နဲ့ တွဲရေးတာ ပိုအဆင်ပြေပါတယ်။

---
# to continue

---
# pandas
```python
!pip install pandas
```
```python
import pandas as pd

df = pd.DataFrame({'name':["Mg Mg","Ko Ko"],'age':[20,30]})
```

---
# df.iloc[]
```python
df.iloc[0] # first row of data frame
```
```python
df['name'] # all value in 'name' column
```
```python
df[df.age > 25] # using condition
```

---
# Graph
```python
import matplotlib.pyplot as plt
import numpy as np

for cur_name in dist_item_name:
	cur_df = sale_item_df[sale_item_df['item_name'] == cur_name]
	print(cur_df.head())
	# we need dist date for analysis
	x = list(set(cur_df["created_date"].to_numpy()))
	# profit must be sum for same date
	y = []
	for cur_x in x:
		temp_y = cur_df[cur_df['created_date']==cur_x]['profit'].to_numpy()
		y.append(np.sum(temp_y))
	#print(x)
	#print(y)
	plt.scatter(x,y)
plt.show()
```