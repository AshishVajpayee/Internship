### Python Basics

#### Simple Print Statement


```python
print('Hello World!!')
```

    Hello World!!
    

#### Printing Multiple Statements


```python
print('This is Print statement')
print("Multiple print statements")
```

    This is Print statement
    Multiple print statements
    

#### Using variable to store Data


```python
name = "Ashish" ## var name holds the value Ashish
age = "22"

print("My Name is " + name + ", I am " + age + " Years old") ## Using + name + to concatenate the print statement with value stored in var 
```

    My Name is Ashish, I am 22 Years old
    

#### Taking user input 


```python
name = input("Enter your Name: ")
print("Hello " + name + "!")
```

    Enter your Name: Ashish
    Hello Ashish!
    

#### Lists Example


```python
friends = ["Akash", "Vishnu", "Karthik", "Vaibhav"] ## Index 0 = Akash, 1 = vishnu, 2 = karthik
friends.sort()
print(friends) ## friends[0] prints Akash, [1:] prints list values from index 1 onwards till n;

```

    ['Akash', 'Karthik', 'Vaibhav', 'Vishnu']
    

#### Tuples Examples


```python
coordinates = (4, 5) ## Tuples are immutable
print(coordinates[0])
```

    4
    

#### Dictionaries


```python
monthConversions = {
    "Jan": "January",
    "Feb": "February",
    "Mar": "March",
}
# Key Value Pairs

##print(monthConversions["Feb"])
print(monthConversions.get("Mar"))

```

    March
    

#### Comments


```python
#This is Comment example
print("Comments for Fun") #This prints out a string 

# Single line Comment
# for multi line comment you need to add # to each line of comment
# first line
#second line..


```

    Comments for Fun
    

#### Casting


```python
a = str(3) # a will be '3'
b = int(3) # b will be 3
c = float(3) # c will be 3.0

print(a)
print(b)
print(c)
```

    3
    3
    3.0
    

#### Get the type of Data type


```python
x = 10
y = "Example"
print(type(x))
print(type(y))
```

    <class 'int'>
    <class 'str'>
    

#### Type Conversion


```python
x = 1   # int 
y = 2.8 # float
z = 1j  # complex

#Convert from int to float:
a = float(x)

b = int(y)

c = complex(x)

print(a)
print(b)
print(c)

print(type(a))
print(type(b))
print(type(c))
```

    1.0
    2
    (1+0j)
    <class 'float'>
    <class 'int'>
    <class 'complex'>
    

#### Random Number


```python
import random

print(random.randrange(1, 10))
```

    6
    

### Python Strings


```python
print("Hello") # Double Quotes works same as single quotes
print('Hello')

a = "Hello !!" #Assign String to a variable
print(a)

b = """ Hello you're in Multiline String
this is the multiline string.
"""    # use three double quotes to write multiline string
print(b)

c = "Hello, World" 
print(c[1]) # Strings are arrays

for x in "banana":
    print(x) # Looping through a string
    
# String Length
print(len(a))

txt = "The best things in life are freebies"
print("free" in txt)

if "free" in txt:
    print("Yes,  'free' is present.")
```

    Hello
    Hello
    Hello !!
     Hello you're in Multiline String
    this is the multiline string.
    
    e
    b
    a
    n
    a
    n
    a
    8
    True
    Yes,  'free' is present.
    

#### Python Slicing Strings


```python
x = "Hello, world!"
print(x[2:5]) # Get the characters from position 2 to 5

print(x[:5]) # Get the characters from the start position 5

print(x[2:]) # Get the characters from position 2, and all the way to end

print(x[-5:-2]) 
```

    llo
    Hello
    llo, world!
    orl
    

#### Python - Modify Strings


```python
a = "Hello, world!  "
print(a.upper()) # built-in method to make string characters to uppercase 

print(a.lower()) # this statement will make string characters to lowercase

print(a.strip()) # returns "Hello, world!"

print(a.replace("H", "T")) # replaces the char H to T

print(a.split(",")) # returns ["Hello", "world!"]


```

    HELLO, WORLD!  
    hello, world!  
    Hello, world!
    Tello, world!  
    ['Hello', ' world!  ']
    

#### String Concatenation


```python
a = "Hello"
b = "World"
c = a + b
print(c)

z = a + " " + b # this will add space between 
print(z)
```

    HelloWorld
    Hello World
    

#### String Format


```python
age = 22
txt = "My name is Ash, and I am {}"
print(txt.format(age)) # As we know we cannot combine strings with numbers. So, to overcome we use format
```

    My name is Ash, and I am 22
    

#### Python - Escape Characters

Code |Result
-----|-----
`\'`| Single Quote
`\\`|Backslash
`\n`|New Line
`\r`| Carriage Return
`\t`| Tab
`\b`|Backspace
`\ooo`|Octal value
`\xhh`|Hex Value



```python
txt = "People of \"India\" ruling on IT Sector" # using Escape Character
print(txt) 
```

    People of "India" ruling on IT Sector
    

#### Python Booleans
In programming you often need to know if an expression is True or False.

You can evaluate any expression in Python, and get one of two answers, True or False.

When you compare two values, the expression is evaluated and Python returns the Boolean answer:


```python
print(10 > 9)
print(10 == 9)
print(10 < 9)
```

    True
    False
    False
    


```python
a = 200
b = 330

if b > a:
  print("b is greater than a")
else:
  print("b is not greater than a")
```

    b is greater than a
    

#### Python Operators
Operators are used to perform operations on variables and values.

In the example below, we use the + operator to add together two values:


```python
print(10 + 9)
```

    19
    

##### Python divides the operators in the following groups:
<ul>
    <li>Arithmetic operators</li>
    <li>Assignment operators</li>
    <li>Comparison operators</li>
    <li>Logical operators</li>
    <li>Identity operators</li>
    <li>Membership operators</li>
    <li>Bitwise operators</li>
</ul>

##### Python Arithmetic Operators
<p>Arithmetic operators are used with numeric values to perform common mathematical operations:</p>

Operator | Name | Example
---------|------|--------
`+`      | Addition| x + y 
`-`      | Substraction | x - y
`*`      | Multiplication | x * y
`/`      | Division | x / y
`%`      | Modulus | x % y
`**`     | Exponential | x ** y
`//`    | Floor Divison | x // y

<p> To get more related to operators visit <a href = "https://www.w3schools.com/python/python_operators.asp">here.</a> </p>


```python
def add(x, y):
    return x+y

def sub(x, y):
    return x-y

def mul(x, y):
    return x*y

def mod(x, y):
    try:
        return x%y
    except:
        print("Enter the Valid Divisor")
        
def div(x, y):
    try:
        return x/y
    except:
        print("Enter the Valid Divisior")
        
num1 = int(input("Enter a number: "))
num2 = int(input("Enter another number: "))

print("The addition of two numbers", num1 ," and ", num2, "is", add(num1, num2))
print("The subtraction of two numbers", num1 ," and ", num2, "is", sub(num1, num2))
print("The multiplication of two numbers", num1 ," and ", num2, "is", mul(num1, num2))
print("The modulus of two numbers", num1 ," and ", num2, "is", mod(num1, num2))
print("The Divison of two numbers", num1 ," and ", num2, "is", div(num1, num2))

```

    Enter a number: 2
    Enter another number: 5
    The addition of two numbers 2  and  5 is 7
    The subtraction of two numbers 2  and  5 is -3
    The multiplication of two numbers 2  and  5 is 10
    The modulus of two numbers 2  and  5 is 2
    The Divison of two numbers 2  and  5 is 0.4
    


```python
num1 = float(input("Enter first number: "))
op = input("Enter operator: ")
num2 = float(input("Enter second number: "))

if op == "+":
    print(num1 + num2)
    
elif op == "-":
    print(num1 - num2)
    
elif op == "*":
    print(num1 * num2)
    
elif op == "/":
    print(num1 / num2)
elif op == "%":
    print(num1 % num2)
else:
    print("Enter valid operator")

```

    Enter first number: 5
    Enter operator: +
    Enter second number: 5
    10.0
    

#### Python Comparision Operators
Comparison operators are used to compare two values:


```python
x = 5
y = 3

print(x == y) # Equal
print(x != y) # Not Equal
print(x > y)  # Greater than
print(x < y)  # Less than
print(x <= y) # Less than or Equal to
print(x >= y) # Greater than or Equal to




```

    False
    True
    True
    False
    False
    True
    

#### Python Logical Operators
Logical operators are used to combine conditional statements:


```python
x = 5

print(x > 3 and x < 10) # returns True because 5 is greater than 3 AND 5 is less than 10

print(x > 3 or x < 4) # returns True because one of the conditions are true (5 is greater than 3, but 5 is not less than 4)

print(not(x > 3 and x < 10)) # returns False because not is used to reverse the result

# and, or, not are the three Logical operators


```

    True
    True
    False
    

#### Python Identity Operators
Identity operators are used to compare the objects, not if they are equal, but if they are actually the same object, with the same memory location:


```python
x = ["Apple", "Google"]
y = ["Apple", "Google"]
z = x

## x is y
print(x is z)

# returns True because z is the same object as x

print(x is y)

# returns False because x is not the same object as y, even if they have the same content

print(x == y)

# to demonstrate the difference betweeen "is" and "==": this comparison returns True because x is equal to y

print("------------------------------------------------------------------------------------")
## x is not y
print(x is not z)

# returns False because z is the same object as x

print(x is not y)

# returns True because x is not the same object as y, even if they have the same content

print(x != y)

# to demonstrate the difference betweeen "is not" and "!=": this comparison returns False because x is equal to y
```

    True
    False
    True
    ------------------------------------------------------------------------------------
    False
    True
    False
    

#### Python Membership Operators
Membership operators are used to test if a sequence is presented in an object:


```python
x = ["apple", "banana"]

print("banana" in x) # returns True because a sequence with the value "banana" is in the list

print("pineapple" not in x) # returns True because a sequence with the value "pineapple" is not in the list

# x in y
# x not in y
```

    True
    True
    

#### Python Lists
Lists are used to store multiple items in a single variable.

Lists are one of 4 built-in data types in Python used to store collections of data, the other 3 are Tuple, Set, and Dictionary, all with different qualities and usage.

Lists are created using square brackets:


```python
fruits = ["apple", "banana", "cherry"]
print(fruits)
```

    ['apple', 'banana', 'cherry']
    

### List comprehension


```python
# For loop
x = [1, 2, 3, 4, 5]
y = []
for item in x:
    if item > 2:
        y.append(item)
print (y)
```

    [3, 4, 5]
    


```python
# List comprehension
y = [item for item in x if item > 2]
print (y)
```

    [3, 4, 5]
    

#### Python Collections (Arrays)
There are four collection data types in the Python programming language:
<ul>
    <li>List is a collection which is ordered and changeable. Allows duplicate members.</li>
    <li>Tuple is a collection which is ordered and unchangeable. Allows duplicate members.</li>
    <li>Set is a collection which is unordered, unchangeable*, and unindexed. No duplicate members.</li>
    <li>Dictionary is a collection which is ordered** and changeable. No duplicate members.</li>
</ul>


```python

```

#### Python - Access List Items


```python
Fruitlist = ["apple", "banana", "cherry"]
print(Fruitlist[1])

```

    banana
    


```python
friends = ["Akash", "Vishnu", "Karthik", "Vaibhav", "Vijay"] ## Index 0 = Akash, 1 = vishnu, 2 = karthik
friends.sort()
print(friends) ## friends[0] prints Akash, [1:] prints list values from index 1 onwards till n;

print(friends[2:]) # Range of Indexes
#Remember that the first item is position 0,
#and note that the item in position 5 is NOT included

if "Karthik" in friends:
    print("Yes, 'Karthik' is in the friends")

```

    ['Akash', 'Karthik', 'Vaibhav', 'Vijay', 'Vishnu']
    ['Vaibhav', 'Vijay', 'Vishnu']
    Yes, 'Karthik' is in the friends
    

#### Python Change List items


```python
friends = ["Akash", "Vishnu", "Karthik", "Vaibhav", "Vijay"] ## Index 0 = Akash, 1 = vishnu, 2 = karthik
friends[1] = "Anand" # changing the value at position 1 vishnu to Anand
print(friends)

#insert new items to the list
friends.insert(2, "Vishal")  # added vishal at index or position 2
print(friends)
```

    ['Akash', 'Anand', 'Karthik', 'Vaibhav', 'Vijay']
    ['Akash', 'Anand', 'Vishal', 'Karthik', 'Vaibhav', 'Vijay']
    

#### Append Items
To add an item to the end of the list, use the append() method:


```python
mylist = ["apple", "banana", "cherry"]

mylist.append("orange") # this will append orange at the end of list

print(mylist)
```

    ['apple', 'banana', 'cherry', 'orange']
    


```python
mylist = ["apple", "banana", "cherry"]
oldlist = ["mango", "pineapple", "papaya"]
mylist.extend(oldlist)# this will merge with mylist

print(mylist)
tuplelist = ("Guvava", "watermelon")
mylist.extend(tuplelist) # this tuple list will merge with mylist
print(mylist)
```

    ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya']
    ['apple', 'banana', 'cherry', 'mango', 'pineapple', 'papaya', 'Guvava', 'watermelon']
    

#### Python - Remove List Items


```python
thislist = ["apple", "banana", "cherry", "papaya", "mango"]
thislist.remove("banana") # it will remove banana from the list
print(thislist)

thislist.pop(1) # this will delete or pop the element form index 1
print(thislist) 

thislist.pop() # this will pop the last element in the list
print(thislist)

del thislist[0] # this will delete the element from index 0
print(thislist)

thislist.clear() # this will clear the list prints empty list
print(thislist)
```

    ['apple', 'cherry', 'papaya', 'mango']
    ['apple', 'papaya', 'mango']
    ['apple', 'papaya']
    ['papaya']
    []
    

#### Loop Through a List
You can loop through the list items by using a for loop:


```python
thislist = ["apple", "banana", "cherry"]
for x in thislist:
  print(x)
```

    apple
    banana
    cherry
    


```python
# Refering to their index numbers [0,1,2]
thislist = ["apple", "banana", "cherry"]
for i in range(len(thislist)):
  print(thislist[i])
```

    apple
    banana
    cherry
    


```python
# Loop through while loop to go through all the index numbers
thislist = ["apple", "banana", "cherry"]
i = 0
while i < len(thislist):
  print(thislist[i])
  i = i + 1 #increment by 1 at each iteration
```

    apple
    banana
    cherry
    


```python
thislist = ["apple", "banana", "cherry"]
[print(x) for x in thislist] # short hand for loop that will print all the list items
```

    apple
    banana
    cherry
    




    [None, None, None]



#### Python - List Comprehension


```python
fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = []

for x in fruits:
  if "a" in x:        # If a is found in any of the list items get added to newlist
    newlist.append(x)

print(newlist) # prints the newlist
```

    ['apple', 'banana', 'mango']
    

#### Sort List


```python
friends = ["Akash", "Vishnu", "Karthik", "Vaibhav", "Vijay", "Anand"] ## Index 0 = Akash, 1 = vishnu, 2 = karthik
friends.sort()
print(friends)
      
friends.sort(reverse = True)
print(friends)

friends2 = ["Akash", "Undertaker", "John", "zak", "Bijay", "Ashley"]
friends2.reverse() #reverse the list of items
print(friends2)
```

    ['Akash', 'Anand', 'Karthik', 'Vaibhav', 'Vijay', 'Vishnu']
    ['Vishnu', 'Vijay', 'Vaibhav', 'Karthik', 'Anand', 'Akash']
    ['Ashley', 'Bijay', 'zak', 'John', 'Undertaker', 'Akash']
    

#### Tuple
- Tuples are used to store multiple items in a single variable.

- Tuple is one of 4 built-in data types in Python used to store collections of data, the other 3 are List, Set, and Dictionary, all with different qualities and usage.

- A tuple is a collection which is ordered and unchangeable.

- Tuples are written with round brackets.


```python
thistuple = ("apple", "banana", "cherry")
print(thistuple)
print(len(thistuple)) # len of the tuple

print(thistuple[1]) # Access tuples 

thistuple1 = ("apple",) # remeber , comma to be consider
print(type(thistuple1))

#NOT a tuple
thistuple3 = ("apple")
print(type(thistuple3))
```

    ('apple', 'banana', 'cherry')
    3
    banana
    <class 'tuple'>
    <class 'str'>
    

#### Convert the tuple to list 


```python
x = ("apple", "banana", "cherry")
y = list(x) # keeping all the values in list method built-in
y[1] = "kiwi" #add kiwi in list y
x = tuple(y) # tuple of y

print(x)
```

    ('apple', 'kiwi', 'cherry')
    


```python
thistuple = ("apple", "banana", "cherry")
y = list(thistuple)
y.append("orange")
thistuple = tuple(y)

print(thistuple)

```

    ('apple', 'banana', 'cherry', 'orange')
    

#### Python Sets


```python
exampleset = {"apple", "banana", "cherry"}
print(exampleset) 
```

    {'banana', 'cherry', 'apple'}
    


```python
thisset = {"apple", "banana", "cherry"}

print(len(thisset))
```

    3
    


```python
thisset = {"apple", "banana", "cherry"}

for x in thisset:
  print(x)
```

    banana
    cherry
    apple
    


```python
thisset = {"apple", "banana", "cherry"}

thisset.add("orange") #add set items

print(thisset)
```

    {'banana', 'cherry', 'apple', 'orange'}
    


```python
thisset = {"apple", "banana", "cherry"}

thisset.remove("banana")

print(thisset)
```

    {'cherry', 'apple'}
    


```python
thisset = {"apple", "banana", "cherry"}

thisset.discard("banana")

print(thisset)
```

    {'cherry', 'apple'}
    

#### Python Dictionaries


```python
thisdict = {
  "brand": "Ford",  # key brand, value Ford
  "model": "Mustang",
  "year": 1964
}
print(thisdict)
```

    {'brand': 'Ford', 'model': 'Mustang', 'year': 1964}
    


```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
print(thisdict["brand"]) # print the brand value of the dictionary
```

    Ford
    


```python
thisdict = {
  "brand": "Ford",
  "model": "Mustang",
  "year": 1964
}
thisdict.update({"year": 2020}) # update year

print(thisdict)
```

    {'brand': 'Ford', 'model': 'Mustang', 'year': 2020}
    


```python
myfamily = {
  "child1" : {
    "name" : "Emil",
    "year" : 2004
  },
  "child2" : {
    "name" : "Tobias",
    "year" : 2007
  },
  "child3" : {
    "name" : "Linus",
    "year" : 2011
  }
}

print(myfamily)
```

    {'child1': {'name': 'Emil', 'year': 2004}, 'child2': {'name': 'Tobias', 'year': 2007}, 'child3': {'name': 'Linus', 'year': 2011}}
    

### Python Conditions and If statements
- Python supports the usual logical conditions from mathematics:

- Equals: `a == b`
- Not Equals: `a != b`
- Less than: `a < b`
- Less than or equal to: `a <= b`
- Greater than: `a > b`
- Greater than or equal to: `a >= b`
- These conditions can be used in several ways, most commonly in "if statements" and loops.

An "if statement" is written by using the if keyword.



```python
# if statement
a = 33
b = 200
if b > a:
  print("b is greater than a")
```

    b is greater than a
    


```python
# elif example
a = 33
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
```

    a and b are equal
    


```python
# else statement
a = 200
b = 33
if b > a:
  print("b is greater than a")
elif a == b:
  print("a and b are equal")
else:
  print("a is greater than b")
```

    a is greater than b
    

#### Nested if


```python
x = 41

if x > 10:
  print("Above ten,")
  if x > 20:
    print("and also above 20!")
  else:
    print("but not above 20.")
```

    Above ten,
    and also above 20!
    


```python
# if statement and comparisions
def max_num(num1, num2, num3):
    if num1 >= num2 and num1 >= num3:
        return num1
    elif num2 >= num1 and num2 >= num3:
        return num2
    else:
        return num3
    
print(max_num(3, 40, 5))
```

    40
    

### Python Loops
- Python has two primitive loop commands:

`while` loops<br>
`for` loops
### The while Loop
- With the while loop we can execute a set of statements as long as a condition is true.


```python
i = 1
while i <= 10: # Until condition is true it keeps executing
    print(i)
    i += 1 # adds 1 to i again goes to condition checks for it and keeps iterating
    
print("Done with Loop")
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    Done with Loop
    


```python
# using break 
i = 1
while i < 6:
  print(i)
  if i == 3:
    break # exit the loop when i is 3
  i += 1
```

    1
    2
    3
    


```python
# using Continue 
i = 0
while i < 6:
  i += 1
  if i == 3:
    continue
  print(i)
```

    1
    2
    4
    5
    6
    


```python
# print the message once Condition is false
i = 1
while i < 6:
  print(i)
  i += 1
else:
  print("i is no longer less than 6")
```

    1
    2
    3
    4
    5
    i is no longer less than 6
    

### Python For Loops
- A `for` loop is used for iterating over a sequence (that is either a list, a tuple, a dictionary, a set, or a string).

- This is less like the `for` keyword in other programming languages, and works more like an iterator method as found in other object-orientated programming languages.

- With the `for` loop we can execute a set of statements, once for each item in a list, tuple, set etc.


```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x)
```

    apple
    banana
    cherry
    


```python
for index in range(5):
    print(index)
    
friends = ["Jim", "John", "Kevin"]
for friend in friends:
    print(friend)
    
for index in range(5):
    if index == 0:
        print("First Iteration")
    else:
        print("Not first")
```

    0
    1
    2
    3
    4
    Jim
    John
    Kevin
    First Iteration
    Not first
    Not first
    Not first
    Not first
    


```python
# break
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  print(x) 
  if x == "banana":
    break
```

    apple
    banana
    


```python
fruits = ["apple", "banana", "cherry"]
for x in fruits:
  if x == "banana":
    continue
  print(x)
```

    apple
    cherry
    


```python
for x in range(6):
  print(x) 
```

    0
    1
    2
    3
    4
    5
    


```python
for x in range(6):
  print(x)
else:
  print("Finally finished!")
```

    0
    1
    2
    3
    4
    5
    Finally finished!
    


```python
adj = ["red", "big", "tasty"]
fruits = ["apple", "banana", "cherry"]

for x in adj:
  for y in fruits:
    print(x, y)
```

    red apple
    red banana
    red cherry
    big apple
    big banana
    big cherry
    tasty apple
    tasty banana
    tasty cherry
    

### Python Functions
- A function is a block of code which only runs when it is called.

- You can pass data, known as parameters, into a function.

- A function can return data as a result.

#### Creating a Function
- In Python a function is defined using the **`def`** keyword:



```python
def my_function():
  print("Hello from a function")

my_function()
```

    Hello from a function
    


```python
def fun(name, age): # def your own Function using def keyword
    print("Hello " + name + ", you are " +str(age))
    
fun("Ashish", 22)
fun("Ram", 22)
```

    Hello Ashish, you are 22
    Hello Ram, you are 22
    

### Python Lambda
- A **`lambda`** function is a small anonymous function.

- A **`lambda`** function can take any number of arguments, but can only have one expression.


```python
x = lambda a : a + 10
print(x(5))
```

    15
    


```python
x = lambda a, b : a * b  # Summarize argument a, b, and c and return the result
print(x(5, 6))
```

    30
    


```python
def myfunc(n):
  return lambda a : a * n

mydoubler = myfunc(2)

print(mydoubler(11))
```

    22
    

### Python Classes and Objects
- Python Classes/Objects
- Python is an object oriented programming language.

- Almost everything in Python is an object, with its properties and methods.

- A Class is like an object constructor, or a "blueprint" for creating objects.


```python
class MyClass:
  x = 5

p1 = MyClass()
print(p1.x)
```

    5
    


```python
class Person:
  def __init__(self, name, age): # Create a class named Person, use the __init__() function to assign values for name and age:
    self.name = name
    self.age = age

p1 = Person("John", 36)

print(p1.name)
print(p1.age)
```

    John
    36
    


```python
# Insert a function that prints a greeting, and execute it on the p1 object:

class Person:
  def __init__(self, name, age):
    self.name = name
    self.age = age

  def myfunc(self):
    print("Hello my name is " + self.name)

p1 = Person("John", 36)
p1.myfunc()
```

    Hello my name is John
    

### Classes and Objects


```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

class Student(Person):
  pass

x = Student("Ashish", "Vajpayee")
x.printname()

```

    Ashish Vajpayee
    


```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)

x = Student("John", "Sena")
x.printname()
```

    John Sena
    


```python
# Creating the class
class Pet(object):
    """Class object for a pet."""

    def __init__(self, species, name):
        """Initialize a Pet."""
        self.species = species
        self.name = name

# Creating an instance of a class
my_dog = Pet(species="dog",
             name="Scooby")
print (my_dog)
print (my_dog.name)
```

    <__main__.Pet object at 0x0000021A707D6D40>
    Scooby
    


```python
# Creating the class
class Pet(object):
    """Class object for a pet."""

    def __init__(self, species, name):
        """Initialize a Pet."""
        self.species = species
        self.name = name

    def __str__(self):
        """Output when printing an instance of a Pet."""
        return f"{self.species} named {self.name}"

    def change_name(self, new_name):
        """Change the name of your Pet."""
        self.name = new_name

# Creating an instance of a class
my_dog = Pet(species="dog", name="Scooby")
print (my_dog)
print (my_dog.name)
```

    dog named Scooby
    Scooby
    


```python
class Person:
  def __init__(self, fname, lname):
    self.firstname = fname
    self.lastname = lname

  def printname(self):
    print(self.firstname, self.lastname)

class Student(Person):
  def __init__(self, fname, lname):
    super().__init__(fname, lname)
    self.graduationyear = 2019

x = Student("Mike", "Olsen")
print(x.graduationyear)
```

    2019
    

#### Python JSON


```python
import json

# some JSON:
x = '{ "name":"John", "age":30, "city":"New York"}'

# parse x:
y = json.loads(x) # Convert JSON to Python

# the result is a Python dictionary:
print(y["age"])

```

    30
    


```python
import json

# a Python object (dict):
x = {
  "name": "John",
  "age": 30,
  "city": "New York"
}

# convert into JSON:
y = json.dumps(x)

# the result is a JSON string:
print(y)
```

    {"name": "John", "age": 30, "city": "New York"}
    

### Python Try Except
- The `try` block lets you test a block of code for errors.

- The `except` block lets you handle the error.

- The `else` block lets you execute code when there is no error.

- The `finally` block lets you execute code, regardless of the result of the `try`- and `except` blocks.


```python
try:
    answer = 10/0
    number = int(input("Enter a number: "))
    print(number)

except ZeroDivisionError:
    print("Divided by Zero")
except ValueError:
    print("invalid input")
except:
    print("Invalid Input")
        
```

    Divided by Zero
    

### Taking User Input


```python
name = input("Enter your Name: ")
print("Hello " + name + "!")
```

    Enter your Name: Ashish
    Hello Ashish!
    


```python

```
