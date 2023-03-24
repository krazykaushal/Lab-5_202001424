## <pre>IT 314 - Software Engineering </pre> 
### Lab 5 : Static Analysis
- Student Name : Kaushal Patel
- Student ID: 202001424
---
### Static analysis tool: **Pylint**


I installed `pylint` extension in VScode.

```
pip install pylint
```
---
## Github Repo used : https://github.com/KaProDes/python3

- Using `kalc.py` as the first step to test **Pylint**:

```python
def main():
	print("Hello, I am the versatile kalc function.")
	print("I won't print anything if I'm imported.")
	print("I will print directly only if I am the base code")
    
def aux():
    print("I am test case print statement.")
    print("My contents will be parsed only if I am explicitly called")

if __name__ == '__main__':
	main()
```
<br/>

> Here we can see the output thrown by **Pylint**

![error1](https://user-images.githubusercontent.com/75678291/227482002-7183e072-e355-42ab-8c04-5f418153beb9.png)

---

- Using `tut12.py` to test **Pylint**
```python
'''The Math module/library in Python3'''

##this is an import statement --
import math
##alternatively we can do a selective import 
from math import sqrt
import math as m

#Lets make use of this sqrt function
y = sqrt(25)
print(y)
print(int(math.sqrt(256)))
z = m.sqrt(54)
print(round(z,3))

#Floor and ceil functions 
print(m.floor(z))
print(m.ceil(z))

#Exponents and Powers
print(2**4)
print(m.pow(4,3))

#Constats from math library
print(m.pi)
print(m.e)

#For more info
##print(help('math'))
```

> Here we can see the output thrown by **Pylint*

![erro2](https://user-images.githubusercontent.com/75678291/227484291-54ddf36e-3e33-41b7-9880-2af08fa66f74.png)

---

- Using `tut14.py` to test **Pylint**:
```python
#Basic syntax of if statements
if True:
    print("This line appears in console!")
    
if False:
    print("This line does not appear in console!")
    
#Checking even and odd 

x = 3
y = 2

if x%2!=0:
    print("x is odd")
    
if y%2==0:
    print("y is even")
    
#Lets use if-else blocks 

z = 87
if z%2==0:
    print(z,"is even")
else:
    print(z,"is odd")
    
#Using elif statements

num = 3
if num == 1:
    print("One")
elif num == 2:
    print("Two")
elif num == 3:
    print("Three")
elif num == 4:
    print("Four")
    
```

> Here we can see the output thrown by **Pylint**

![error3](https://user-images.githubusercontent.com/75678291/227485359-a7c47ff8-791e-4ca5-b6bf-e1cc74a5036a.png)

---

## Understanding of Errors:

- **C0303** - Trailing Whitespaces

  Actual code lines do not have trailing whitespaces. These are for indentation. Does not break the code. It is a suggestion for better readability of code.
  
- **C0103** - Invalid Name

  Naming convention is not followed for these methods. Should be updated for uniformity.

- **C0114** - Missing module docstring

  A Python module should have a docstring, explaining what the module does, what it provides, and examples of how to use the classes.
  
- **W0404** - reimported

  Used when a module is imported more than once.
  
- **W0311** - bad-indentation

  Used when an unexpected number of indentation's tabulations or spaces has been found.
  
- **W0125** - using-constant-test

  Emitted when a conditional statement (If or ternary if) uses a constant value for its test. This might not be what the user intended to do.




