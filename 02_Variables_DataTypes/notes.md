# Module 02 – Variables & Data Types (Detailed Notes)

---

## 1. Introduction

Variables and data types are the building blocks of any programming language.  
They determine **how data is stored**, **how it behaves**, and **how Python 
interprets it during execution**. Python is dynamically typed, meaning you don't 
need to explicitly declare the data type of a variable.

Example:
```python
x = 10
y = "Hello"

Python automatically understands that:

x is an integer

y is a string

2. What is a Variable?

A variable is a name that refers to a value stored in memory.
Think of it as a labelled box storing some information.

Properties

Variables are created when you assign a value.

They can store any type of data.

The type can change during execution (dynamic typing).

Example:
a = 5
a = "Python"     # new type in same variable

3. Rules for Naming Variables
| Rule                                    | Example          |
| --------------------------------------- | ---------------- |
| Must start with a letter or underscore  | `name`, `_age`   |
| Cannot start with a digit               | ❌ `1var`         |
| Can contain letters, digits, underscore | `student_1`      |
| Case-sensitive                          | `age` ≠ `Age`    |
| No spaces                               | ❌ `student name` |


Avoid using keywords such as:
if, else, while, break, class, import, def

4. Python Data Types (Core)

Python has several built-in data types. For this module we focus on:

4.1 Integer (int)

Whole numbers, positive or negative.

x = 10
y = -5

4.2 Float (float)

Decimal numbers.

pi = 3.14

4.3 String (str)

Sequence of characters enclosed in ' ' or " ".

name = "Pankaj"
msg = 'Hello'

4.4 Boolean (bool)

Stores True or False.

is_active = True
is_admin = False

5. Checking Data Type

Use the type() function:

x = 10
print(type(x))


Output:

<class 'int'>

6. Type Conversion (Casting)
Explicit casting:
x = int("10")
pi = float("3.14")
name = str(100)

Implicit casting:

Python automatically promotes values.

a = 5
b = 2.0
result = a + b     # becomes float

7. String Operations

Strings are extremely powerful.

Concatenation:
s = "Hello" + " Python"

Repetition:
s = "Hi!" * 3

Indexing:
H  e  l  l  o
0  1  2  3  4

word = "Hello"
print(word[1])   # e

Slicing:
msg = "Python"
print(msg[0:3])   # Pyt

8. Getting Input from User

Use:

name = input("Enter your name: ")
age = int(input("Enter your age: "))

9. Memory Concept (Important)

Python stores variables as references.

Example:

x = 10
y = x


Both point to the same memory address for value 10.

Use id():

print(id(x))
print(id(y))

10. Mutability

Immutable types: int, float, bool, str, tuple
→ Cannot be changed in-place

Mutable types: list, dict, set
→ Can be changed

Example:

name = "Pankaj"
# name[0] = "R"   # ❌ ERROR (immutable)

11. Summary Table
| Type  | Example | Mutable? |
| ----- | ------- | -------- |
| int   | 10      | No       |
| float | 3.14    | No       |
| bool  | True    | No       |
| str   | "Hello" | No       |
| list  | [1,2,3] | Yes      |
| dict  | {"a":1} | Yes      |

12. Real-World Uses

Variables store sensor data in IoT

Strings store user input, API data

Boolean values decide conditions

Floats used for scientific calculations

Understanding variables is critical for writing efficient programs.


---

# 📄 `02_Variables_DataTypes/examples.py`

```python
# Examples – Variables and Data Types

# Integer
age = 25
print("Age:", age)

# Float
temperature = 36.6
print("Temperature:", temperature)

# String
name = "Pankaj"
print("Hello,", name)

# Boolean
is_student = True
print("Student?", is_student)

# Type checking
print(type(name))

# Type conversion
x = "100"
y = int(x)
print("Converted:", y)

# Input example
city = input("Enter your city: ")
print("You live in:", city)
