# caalamitaas

# Update and upgrade all existing system packages
```bash
pkg update && pkg upgrade -y
```

# Install the Python interpreter
```bash
pkg install python -y
```

# Verify that Python installed successfully and check the version
```bash
python --version
```

# 'w' stands for write mode. This creates the file if it doesn't exist.
```python
with open("log.txt", "w") as file:
    file.write("DevOps System Log: Script executed successfully on Termux!\n")
    file.write("Status: Active and learning.\n")

print("File 'log.txt' has been automatically created and written to!")
```

# Linux, Python and DevOps Reference

## 1. Directory Navigation and File Management
```bash
# Print Working Directory
pwd

# List contents of current folder
ls

# List all files including hidden files
ls -a

# Move into a specific folder
cd folder_name

# Go back one folder level up
cd ..

# Go back to home directory
cd ~

# Create a new folder
mkdir new_folder_name

# Delete an empty folder
rmdir folder_name

# Delete a file permanently
rm file_name.py

# Force delete a folder and everything inside it
rm -rf folder_name

# Clear your terminal screen
clear
```
# Linux, Python and DevOps Reference

## 1. Directory Navigation and File Management
```bash
# Print Working Directory
pwd

# List contents of current folder
ls

# List all files including hidden files
ls -a

# Move into a specific folder
cd folder_name

# Go back one folder level up
cd ..

# Go back to home directory
cd ~

# Create a new folder
mkdir new_folder_name

# Delete an empty folder
rmdir folder_name

# Delete a file permanently
rm file_name.py

# Force delete a folder and everything inside it
rm -rf folder_name

# Clear your terminal screen
clear
```

---

## 2. Programming Language Installations
```bash
# Install Node.js and NPM
pkg install nodejs -y

# Install C and C++ Compiler
pkg install clang -y

# Compile a C++ file named main.cpp into a program named app
clang++ main.cpp -o app

# Run compiled C++ application
./app

# Install Git
pkg install git -y

# Download a repository from GitHub to local device
git clone https://github.com
```

---

## 3. Linux Distros Inside Termux
```bash
# Install distribution management tool
pkg install proot-distro -y

# List available Linux operating systems
proot-distro list

# Install Ubuntu Server Core
proot-distro install ubuntu

# Log into Ubuntu container
proot-distro login ubuntu

# Exit back to Termux
exit
```

---

## 4. Python File Operations

### Text File Operations
```python
# Write Mode (creates a new file or overwrites)
with open("notes.txt", "w") as file:
    file.write("Learning Linux infrastructure daily.\n")

# Append Mode (adds text to the bottom)
with open("notes.txt", "a") as file:
    file.write("Adding a secondary automation log step.\n")

# Read Mode (reads text out)
with open("notes.txt", "r") as file:
    content = file.read()
    print(content)
```

### JSON Configuration Operations
```python
import json

# Python Dictionary configuration
server_config = {
    "server_name": "Nvidia-Cluster-01",
    "ip_address": "192.168.1.50",
    "status": "Online",
    "ports_open":
}

# Save Python data into a JSON file
with open("config.json", "w") as json_file:
    json.dump(server_config, json_file, indent=4)

# Load and parse data from a JSON file
with open("config.json", "r") as json_file:
    loaded_data = json.load(json_file)
    print("Target IP:", loaded_data["ip_address"])
```

### Time Delays
```python
import time

print("Starting server deployment sequence...")
# Wait exactly 3 seconds
time.sleep(3)
print("Deployment completed successfully!")
```

# Python Core Reference Guide

A complete, clean, and comprehensive reference guide containing all Python keywords and built-in functions. 

---

## 1. Python Keywords (35)
Keywords are the reserved, foundational words that define the syntax, structure, and rules of the Python language. They cannot be used as regular variable or function names.

| Keyword | Description | Code Example |
| :--- | :--- | :--- |
| `False` | Boolean value representing logical falsity. | `status = False` |
| `None` | A special constant representing the absence of a value or a null value. | `result = None` |
| `True` | Boolean value representing logical truth. | `status = True` |
| `and` | A logical operator that returns `True` only if both expressions are true. | `if x > 0 and y > 0:` |
| `as` | Used to create an alias while importing a module or handling an exception. | `import math as m` |
| `assert` | Used for debugging; tests if a condition is true, raising an error if it fails. | `assert x == 5, "x must be 5"` |
| `async` | Declares a function as an asynchronous coroutine. | `async def fetch_data():` |
| `await` | Suspends execution of an async coroutine until the awaited task finishes. | `data = await fetch_data()` |
| `break` | Terminates the current loop immediately and transfers execution outside it. | `for i in range(10): break` |
| `class` | Defines a new user blueprint for creating objects. | `class Dog:` |
| `continue` | Skips the remaining code inside a loop for the current iteration. | `for i in range(5): continue` |
| `def` | Declares a user-defined function. | `def greet():` |
| `del` | Deletes a reference to an object, variable, or item in a collection. | `del user_list[0]` |
| `elif` | Short for "else if"; tests a conditional path if previous conditions failed. | `elif x == 2:` |
| `else` | Executes a block of code if all preceding conditions evaluate to false. | `else: print("Fallback")` |
| `except` | Catches and handles specific exceptions raised within a `try` block. | `except ValueError:` |
| `finally` | Executes a block of code after `try/except`, regardless of errors. | `finally: file.close()` |
| `for` | Creates an iterative loop to step over a sequence or collection. | `for item in items:` |
| `from` | Used to import specific parts, attributes, or functions from a module. | `from math import pi` |
| `global` | Declares that a variable inside a function is bound to the global scope. | `global total_count` |
| `if` | Begins a conditional statement block to evaluate a boolean expression. | `if x > 10:` |
| `import` | Links and includes an external module or library inside the script. | `import os` |
| `in` | Checks if a specific value exists inside a sequence or iterable collection. | `if "a" in "apple":` |
| `is` | Tests object identity to determine if two variables point to the exact same object. | `if x is None:` |
| `lambda` | Declares a small, anonymous, one-line inline function. | `square = lambda x: x * x` |
| `nonlocal` | Declares that a variable belongs to the nearest enclosing parent scope. | `nonlocal outer_var` |
| `not` | A logical operator that inverts the boolean value of an expression. | `if not system_ready:` |
| `or` | A logical operator that returns `True` if at least one expression is true. | `if x > 5 or y > 5:` |
| `pass` | A null statement that acts as a placeholder where syntax requires code. | `def placeholder(): pass` |
| `raise` | Deliberately triggers a specific exception or error during execution. | `raise ValueError("Invalid entry")` |
| `return` | Exits a function and passes a specific value back to the caller. | `return result` |
| `try` | Wraps a block of code to test for and capture runtime errors. | `try: x = 1 / 0` |
| `while` | Creates a loop that continues to run as long as its condition stays true. | `while active:` |
| `with` | Wraps execution with a context manager to automate resource cleanup. | `with open('file.txt') as f:` |
| `yield` | Pauses a function and returns a generator value instead of a static exit. | `yield sequence_item` |

---

## 2. Built-In Functions (71)
These are utility functions available globally in Python without importing any external packages.

### Data Type Conversions & Casting

| Function | Description | Code Example |
| :--- | :--- | :--- |
| `bool(x)` | Converts a value to its corresponding boolean (`True` or `False`). | `bool(1) # True` |
| `bytearray(x)` | Creates and returns a mutable sequence of integers in the range 0 <= x < 256. | `ba = bytearray(5)` |
| `bytes(x)` | Creates and returns an immutable sequence of integers in the range 0 <= x < 256. | `b = bytes([65, 66])` |
| `chr(i)` | Returns the string character corresponding to an integer Unicode code point. | `chr(97) # 'a'` |
| `complex(r, i)` | Instantiates a complex number with a real and an imaginary component. | `c = complex(2, 3)` |
| `dict(x)` | Instantiates a dictionary collection mapped via key-value pairings. | `d = dict(a=1, b=2)` |
| `float(x)` | Converts an integer or valid numeric string into a decimal floating-point number. | `f = float("3.14")` |
| `frozenset(x)` | Returns an immutable, unmodifiable version of a Python set collection. | `fs = frozenset([1, 2])` |
| `hex(x)` | Converts an integer number into its equivalent lower-case hexadecimal string. | `hex(255) # '0xff'` |
| `int(x)` | Converts a float or valid string character sequence into a whole integer. | `num = int("42")` |
| `list(x)` | Converts an iterable collection into an ordered, modifiable list array. | `lst = list((1, 2))` |
| `memoryview(x)` | Creates a memory view object allowing safe access to internal buffer data. | `mv = memoryview(b'xyz')` |
| `oct(x)` | Converts an integer number into its equivalent octal string representation. | `oct(8) # '0o10'` |
| `ord(c)` | Returns an integer representing the Unicode character code of a string symbol. | `ord('a') # 97` |
| `set(x)` | Formats an iterable into a collection of unique, unordered items. | `s = set([1, 1, 2])` |
| `str(x)` | Converts a target object or numeric data into a text string format. | `text = str(100)` |
| `tuple(x)` | Converts an iterable collection into an immutable ordered sequence. | `t = tuple([1, 2])` |

### Math & Numeric Operations

| Function | Description | Code Example |
| :--- | :--- | :--- |
| `abs(x)` | Returns the absolute numeric value of a specific number, removing signs. | `abs(-5) # 5` |
| `divmod(a, b)` | Takes two numbers and returns a tuple containing their quotient and remainder. | `divmod(7, 3) # (2, 1)` |
| `max(x)` | Scans a collection or arguments to find and return the largest item. | `max(1, 5, 2) # 5` |
| `min(x)` | Scans a collection or arguments to find and return the smallest item. | `min(1, 5, 2) # 1` |
| `pow(x, y)` | Raises a base number $x$ to the power of exponent $y$ ($x^y$). | `pow(2, 3) # 8` |
| `round(n, d)` | Rounds a float value to a specific number of decimal places. | `round(3.14159, 2) # 3.14` |
| `sum(i)` | Adds all numerical elements inside an iterable collection together. | `sum([1, 2, 3]) # 6` |

### Collections & Sequence Handling

| Function | Description | Code Example |
| :--- | :--- | :--- |
| `all(i)` | Returns `True` if every single element inside an iterable evaluates to true. | `all([True, True]) # True` |
| `any(i)` | Returns `True` if at least one element inside an iterable evaluates to true. | `any([False, True]) # True` |
| `enumerate(i)` | Takes a collection and returns it as an indexed sequence pairing counters to items. | `enumerate(['a', 'b'])` |
| `filter(f, i)` | Extracts elements from a collection that pass a specific filtering condition. | `filter(lambda x: x>0, lst)` |
| `iter(x)` | Returns an iterator object for a target collection to step through elements. | `it = iter([1, 2])` |
| `len(x)` | Evaluates and returns the exact item count or length of a collection. | `len("hello") # 5` |
| `map(f, i)` | Applies a specified function to every individual item inside an iterable. | `map(str, [1, 2])` |
| `next(i)` | Retrieves the next sequential item from an active iterator object. | `next(it)` |
| `range(s, e)` | Generates an immutable sequence of numbers between defined start and endpoints. | `range(0, 10)` |
| `reversed(s)` | Returns a reversed iterator sequence sequence for a collection. | `reversed([1, 2, 3])` |
| `slice(s, e)` | Creates a slice object specifying how to slice a sequence or string. | `s = slice(0, 2)` |
| `sorted(i)` | Generates a brand new sorted list from the items of any iterable collection. | `sorted([3, 1, 2])` |
| `zip(a, b)` | Aggregates multiple iterables into tuples based on index matching. | `zip([1, 2], ['a', 'b'])` |

### Object Inspection & Introspection

| Function | Description | Code Example |
| :--- | :--- | :--- |
| `callable(x)` | Returns `True` if the target object can be executed like a function. | `callable(print) # True` |
| `dir(x)` | Returns a list of valid attributes and method names available for an object. | `dir([])` |
| `format(v, f)` | Formats a value into a specific string format representation. | `format(0.5, '%') # '50.0000%'` |
| `hash(x)` | Computes and returns the fixed numeric hash value of an immutable object. | `hash("text")` |
| `help(x)` | Invokes the interactive built-in terminal help and documentation engine. | `help(str)` |
| `id(x)` | Returns the exact unique integer memory address identification identity of an object. | `id(obj)` |
| `isinstance(o, c)`| Checks if an object is an instance or subclass of a target type class. | `isinstance(5, int) # True` |
| `issubclass(c, p)`| Checks if a target class is a direct child or subclass of a parent class. | `issubclass(bool, int)` |
| `locals()` | Returns a dictionary representing the current active local symbol table. | `locals()` |
| `globals()` | Returns a dictionary representing the current active global symbol table. | `globals()` |
| `object()` | Generates a blank, featureless object serving as the base for all classes. | `obj = object()` |
