# Python Basics for Data Science

### Python Intro
- General purpose: build anything
- Open Source, Free
- Python packages -also for data science -Many applications and fields
- Version 3.x

### Python Script
- text files (.py)
- contain list of python commands

### Print

```bash
print()
print([1 + 2, "a" * 5, 3])
```

### Variables and types

```bash
height = 117.88
type(height) => float
```

### Type Conversions

```bash
str()
int()
float()
bool()
```

### List
- can contain same + different types
- can contain list of list

```bash
house = [["hallway", hall],
         ["kitchen", kit]]
house[1][0]

Subsetting list
------------------
list = ["a", 1, "b", 2]
list[2]
list[-1]

Slicing
------------------
list = ["a", 1, "b", 2]
list[0:2] => start: inclusive, end: exclusive => ["a", 1]
list[:2] => start: from 0
list[2:] => start: from 2 to end

changing list
------------------
list[2] = 1.89
list[0:2] = ["x", 1.74]
list.append('me')

Adding & removing from list
------------------
list + ["m", 2.75] => ["a", 1, "b", 2, "m", 2.75]
del(list[2])

Copy by reference
------------------
x= [1,4,9]
y=x

Copy by value
------------------
y= list(x)
y= x[:]
```

### Write commands on same line
```bash
The ; sign is used to place commands on the same line.
e.g. del(areas[10]); del(areas[11])
```

### Functions
- piece of reusable code
- solves particular task
- call function instead of writing code 

```bash
max(ageList)
round(1.68,1) => 1.7
round(1.68) => 2
len(list) => return array length
pow(base, exp, mod [OPTIONAL])
help(round)

sorted(full, reverse=True) => providing name variable as a parameter which is third argument of function
```

### Methods
- everything you define is object e.g string, float, list
- functions that belong to objects are called methods

```bash
e.g. 
--str methods capitalize(), replace()
---sister = 'liz'
---sister.capitalize() => 'Liz'
---sister.replace('z', 'sa') => 'Lisa'

--float methods bit_length(), conjugate()

--list methods index(), count(), append()
---list.index("mom")
---list.count(1.73)
---list.append(1) => append 1 at the end
---list.remove('a') => remove first element of a list that matches the input
---list.reverse() => reverse order of list; not asc/desc
```

### Packages 
- directory of python scripts
- each script = module

```bash
NumPy => work with arrays
Matplotlib => for data visualization
scikit-learn => for machine learning
```

```bash
Install packages
------------------
download package manager => pip or get-pip.py
from cmd: 
    python3 get-pip.py
    pip3 install numpy

Import packages
------------------
import numpy

Use: numpy.array([1,2,3])

import numpy as np
np.array([1,2,3])

from numpy import array
array([1,2,3])
```

### NumPy

- Numeric Python
- alternative to python list: numpy array
- calculations over entire arrays
- east and fast

```bash
list + list => concat lists
numpy_array + numpy_array => perform addition on each element of two lists


Subsetting numpy
------------------
list = array([1, 11, 23, 45, 60])
list[1]
list > 23 => will return array([False, False, True, True, True])
list[list < 23] => array([1, 11])
```

### 2D NumPy Arrays

```bash
np_2d = np.array([[1,2],[3,4]])
np_2d.shape => (2,2) # 2 rows, 2 columns

if any element is string then all elements will be converted to string to make list homogeneous

np_2d[0][1] => 2
np_2d[0,1] => 2


np_2d = np.array([[1,2,1.74,5],[3,4,20.5,18.9]])

np_2d[:, 1:3] => will return 1 & 2 columns from each row => array([[2,1.74], [4,20.5]])
np_2d[1, :] => will return all columns from 1 row => array([3,4,20.5,18.9])
```

### Basic Statistics Using Numpy (Data Analysis)

```bash
np.mean(np_city[:,0])
np.median(np_city[:,0])
np.corrcoef(np_city[:,0], np_city[:,1]) => to check height and weight are corelated
np.std(np_city[:,0]) => for standard deviation

sum(), sort()
```