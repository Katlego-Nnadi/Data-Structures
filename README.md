# Data-Structures

## Table of Contents

- [Data Structures](#Data-Structures)
- [Python Lists](#Python-Lists)
- [Errors and Exceptions](#Errors-and-Exceptions)
- [Classes](#Classes)


## Data-Structres
Using Lists as Stacks and Queues:

Stacks: Lists can be used as stacks using the append() method to push elements onto the stack and pop() method to remove the last element.
Queues: Collections module provides the deque class that can efficiently implement a queue using append() for enqueue and popleft() for dequeue operations.
List Comprehensions:

A concise way to create lists in Python.
It provides a compact syntax for creating lists based on existing iterables or sequences.
Example: [x**2 for x in range(10)] generates a list of squares of numbers from 0 to 9.
The delete Statement:

There is no explicit delete statement in Python. Instead, you can use the del statement to remove items from lists or variables from memory.
Tuples and Sequences:

Tuples are immutable sequences, and lists are mutable sequences.
Tuples are created using parentheses, e.g., t = (1, 2, 3).
Sequences in Python include both lists and tuples.
Sets:

Sets are unordered collections of unique elements.
Created using curly braces {} or the set() constructor.
Supports set operations like union, intersection, and difference.
Looping Techniques:

Python provides various looping techniques, including for loops, while loops, and iterating over elements in a sequence using for ... in.
The range() function is often used in loops to generate a sequence of numbers.
Comparing Sequences and Other Types:

Comparison operators (==, !=, <, >, <=, >=) can be used to compare sequences and other data types.
Sequences like lists and tuples can be compared element-wise.
Different data types may have specific comparison rules based on their nature.
These concepts are fundamental to working with data structures, loops, and comparisons in Python programming.

## Python_Lists
Certainly! Here's a brief overview of various operations related to lists in Python:

### Creating a List:

To create a list in Python, you can use square brackets `[]` and separate elements with commas.

```python
my_list = [1, 2, 3, 'hello', True]
```

### Accessing List Elements:

You can access elements in a list using indexing. The index starts from 0.

```python
first_element = my_list[0]  # Access the first element
second_element = my_list[1]  # Access the second element
```

### Negative Indexing:

You can also use negative indexing to access elements from the end of the list.

```python
last_element = my_list[-1]  # Access the last element
second_last_element = my_list[-2]  # Access the second last element
```

### Slicing Lists:

You can use slicing to extract a portion of the list.

```python
subset = my_list[1:4]  # Elements from index 1 to 3
```

### Adding/Changing List Elements:

- **Adding elements:**
  ```python
  my_list.append(4)  # Adds 4 to the end of the list
  ```

- **Changing elements:**
  ```python
  my_list[0] = 'new_value'  # Changes the first element
  ```

### Deleting/Removing List Elements:

- **Deleting by index:**
  ```python
  del my_list[2]  # Removes the element at index 2
  ```

- **Removing by value:**
  ```python
  my_list.remove('hello')  # Removes the first occurrence of 'hello'
  ```

### Python List Methods:

There are various built-in methods for lists, such as `append()`, `extend()`, `insert()`, `pop()`, `clear()`, `index()`, `count()`, `sort()`, and `reverse()`.

### List Comprehension:

List comprehensions provide a concise way to create lists.

```python
squares = [x**2 for x in range(5)]  # Creates a list of squares from 0 to 4
```

### Other List Operations:

- **Finding the length:**
  ```python
  length = len(my_list)
  ```

- **Checking membership:**
  ```python
  is_present = 'hello' in my_list
  ```

### Iterating Through a List:

You can iterate through the elements of a list using a `for` loop.

```python
for element in my_list:
    print(element)
```

These operations cover the basic functionalities of working with lists in Python.

## Errors and Exceptions
Certainly! Here's a summary of concepts related to errors and exceptions in Python:

### Errors:

In Python, errors are of two types:

1. **Syntax Errors:**
   - Occur when the code violates the syntax rules of Python.
   - The code will not run until the syntax error is fixed.

2. **Runtime Errors (Exceptions):**
   - Occur during the execution of the program.
   - Examples include division by zero (`ZeroDivisionError`), accessing an index that doesn't exist (`IndexError`), etc.

### Exceptions:

Exceptions are events that occur during the execution of a program that disrupts the normal flow of instructions.

### Handling Exceptions:

Use `try`, `except`, `else`, and `finally` blocks to handle exceptions:

```python
try:
    # Code that may raise an exception
    result = x / y
except ZeroDivisionError:
    # Handle division by zero
    print("Error: Division by zero!")
else:
    # Executed if no exception is raised
    print("Result:", result)
finally:
    # Always executed, used for cleanup actions
    print("Cleanup")
```

### Raising an Exception:

Use the `raise` statement to raise an exception manually:

```python
if x < 0:
    raise ValueError("x should be non-negative")
```

### The `AssertionError` Exception:

Raise an `AssertionError` exception when an assert statement fails:

```python
assert condition, "Error message"
```

### The `try` and `except` Block:

The `try` block contains the code that might cause an exception, and the `except` block contains the code to handle the exception:

```python
try:
    # Code that may raise an exception
except SomeException:
    # Code to handle the exception
```

### User-Defined Exceptions:

Define custom exceptions by creating a new class that inherits from the `Exception` class:

```python
class MyCustomError(Exception):
    pass

# Raise the custom exception
raise MyCustomError("This is a custom error")
```

### Defining Clean-Up Actions:

Use the `finally` block to define clean-up actions that will be executed no matter what:

```python
try:
    # Code that may raise an exception
except SomeException:
    # Code to handle the exception
finally:
    # Code that will always be executed
```

These concepts help in understanding how to handle errors and exceptions gracefully in Python, improving the robustness of your code.

## Classes
Certainly! Here's a summary of concepts related to classes and objects in Python:

### Classes:

1. **Class Definition Syntax:**
   - Classes are defined using the `class` keyword.
   - The body of the class contains attributes (variables) and methods (functions).
   - Example:
     ```python
     class MyClass:
         attribute = "value"
         
         def method(self):
             print("This is a method.")
     ```

2. **Class Objects:**
   - A class is an object itself.
   - Can be assigned to variables and passed as arguments to functions.
   - Example:
     ```python
     obj = MyClass()
     ```

3. **Instance Objects:**
   - Instances are created from a class and represent individual objects.
   - Each instance has its own set of attributes.
   - Example:
     ```python
     instance = MyClass()
     ```

4. **Method Objects:**
   - Methods are functions defined within a class.
   - They have access to the instance and its attributes through the `self` parameter.
   - Example:
     ```python
     instance.method()
     ```

### Names and Objects:

1. **Names:**
   - Names in Python refer to objects.
   - Assigning a value to a name binds the name to the object.

2. **Objects:**
   - Everything in Python is an object, including numbers, strings, functions, and classes.
   - Objects have a type and can be manipulated using methods.

### Python Scopes and Namespaces:

1. **Scope:**
   - The scope is the region of a program where a namespace can be accessed directly.
   - Python follows the LEGB (Local, Enclosing, Global, Built-in) scope resolution rule.

2. **Namespaces:**
   - A namespace is a mapping of names to objects.
   - Each function, module, and class has its own namespace.
   - Namespaces help in avoiding naming conflicts.

### Class and Instance Variables:

1. **Class Variables:**
   - Variables shared among all instances of a class.
   - Defined outside any method in the class.
   - Example:
     ```python
     class MyClass:
         class_variable = "shared_value"
     ```

2. **Instance Variables:**
   - Variables specific to an instance of a class.
   - Defined in the `__init__` method.
   - Example:
     ```python
     class MyClass:
         def __init__(self, instance_variable):
             self.instance_variable = instance_variable
     ```

### Random Remarks:

### 1. **Inheritance:**
   - Classes can inherit attributes and methods from other classes.

### 2. **Encapsulation:**
   - The concept of bundling data and methods that work on that data within a single unit, i.e., a class.

### 3. **Polymorphism:**
   - Objects can take on more than one form depending on the context.

### 4. **Duck Typing:**
   - Objects are defined by their behavior rather than their class or type.

Understanding these concepts is crucial for effective use of object-oriented programming in Python. They form the basis for creating modular, reusable, and maintainable code.
