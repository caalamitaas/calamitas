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
# =====================================================================
# TERMUX PYTHON CALCULATOR - REFERENCE GUIDE
# =====================================================================

# ---------------------------------------------------------------------
# 1. FUNCTION DEFINITIONS ('def')
# ---------------------------------------------------------------------
# 'def' stands for define. It creates a reusable code block (a function).
# The words inside the parentheses (x, y) are placeholders called parameters.
# 'return' sends the final calculated answer back to the main program.

def add(x, y):
    return x + y  # Adds the two numbers together

def subtract(x, y):
    return x - y  # Subtracts y from x

def multiply(x, y):
    return x * y  # Multiplies the two numbers (* is the multiplication symbol)

def divide(x, y):
    # This 'if' check is critical. If a computer divides by zero, it crashes.
    if y == 0:
        return "Error: Cannot divide by zero!"
    return x / y  # Divides x by y (/ is the division symbol)


# ---------------------------------------------------------------------
# 2. THE MAIN LOOP ('while')
# ---------------------------------------------------------------------
# 'while True' creates an infinite loop. Because 'True' is always true,
# the code inside this block will repeat forever until we explicitly stop it.

while True:
    print("\n--- Termux Python Calculator ---")
    print("Enter '+', '-', '*', '/' or 'exit' to quit.")
    
    # 'input()' pauses the program and waits for the user to type text.
    # '.strip()' automatically chops off accidental spaces typed at the start/end.
    operator = input("Choose an operation: ").strip()
    
    # -----------------------------------------------------------------
    # 3. CONDITIONAL LOGIC ('if', 'elif', 'else')
    # -----------------------------------------------------------------
    # 'if' checks if a condition is true. 
    # '.lower()' converts text to lowercase so 'EXIT' or 'Exit' still works.
    if operator.lower() == 'exit':
        print("Goodbye!")
        break  # 'break' immediately stops and exits the closest 'while' loop.
        
    # 'not in' checks if the user's input matches anything inside the list [].
    if operator not in ['+', '-', '*', '/']:
        print("Invalid operator! Please try again.")
        continue  # 'continue' skips the rest of the code below and restarts the loop.

    # -----------------------------------------------------------------
    # 4. ERROR HANDLING ('try', 'except')
    # -----------------------------------------------------------------
    # 'try' lets you test a block of code for errors while it runs.
    try:
        # 'float()' converts text input strings into mathematical decimal numbers.
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
    except ValueError:
        # If the user types letters instead of a number, a ValueError occurs.
        # This 'except' block catches it cleanly so the program doesn't crash.
        print("Invalid input! Please enter numbers only.")
        continue  # Restarts the calculator loop back at the operator select screen.

    # -----------------------------------------------------------------
    # 5. ROUTING LOGIC & EXECUTION
    # -----------------------------------------------------------------
    # 'elif' stands for 'else if'. It runs only if the previous 'if' was false.
    if operator == '+':
        result = add(num1, num2)       # Calls the 'add' function from line 10
    elif operator == '-':
        result = subtract(num1, num2)  # Calls the 'subtract' function from line 13
    elif operator == '*':
        result = multiply(num1, num2)  # Calls the 'multiply' function from line 16
    elif operator == '/':
        result = divide(num1, num2)    # Calls the 'divide' function from line 19
    
    # The 'f' before the quotes means "Format String". 
    # It allows you to place Python variables directly inside curly brackets {} text.
    print(f"Result: {result}")
    # Python Core Commands & Keywords Cheat Sheet

### 1. Structure & Reusability
*   **`def` (Define):** Tells Python you are building a custom tool, function, or "recipe". It saves the logic into the system memory but does not execute it until you call its exact name later in the code.
*   **`return`:** The exit gate of a function. It takes whatever result or value was calculated inside a `def` block and shoots it back out to the main script where the function was called.

### 2. Loop Control
*   **`while True:`** Creates an infinite loop. Because the condition `True` never changes, it forces the code inside it to repeat forever. This is how you keep interactive terminal tools running without closing after a single action.
*   **`break`:** The kill switch for loops. It immediately shatters the closest `while` or `for` loop and forces the program to skip to the code underneath the loop.
*   **`continue`:** The rewind button for loops. It tells Python to stop running the current loop iteration immediately, skip any code left beneath it, and jump straight back to the very top of the loop to start fresh.

### 3. Making Decisions
*   **`if`:** The primary condition tester. It evaluates if a statement is true (e.g., `if user_input == 'yes':`). If it is true, it executes the code indented directly under it.
*   **`elif` (Else If):** The secondary tester. It provides an extra condition to check *only* if the previous `if` statement turned out to be false. You can chain as many `elif` blocks together as you need.
*   **`else`:** The final catch-all safety net. It requires no conditions and executes automatically if every single `if` and `elif` block above it fails.

### 4. Code Protection & Input Handling
*   **`try`:** A protective shield for risky actions. It alerts Python to watch a specific block of code for unexpected errors while it executes.
*   **`except`:** The emergency safety protocol. If the code inside the `try` block crashes (like a `ValueError` when trying to turn letters into numbers), the `except` block catches the error cleanly and runs backup instructions instead of letting the program crash.
*   **`float()`:** Data type converter. By default, `input()` stores everything as literal text (a string). `float()` converts that text into actual math-compatible decimal numbers.
*   **`.strip()`:** Text cleaner. A string utility method that slices off accidental blank spaces or accidental formatting indents typed at the very beginning or very end of user input text.
*   **`.lower()`:** Text standardizer. Forces any text string to convert entirely to lowercase characters so that user variations (like "EXIT", "Exit", or "exiT") match a single keyword standard.
*   
