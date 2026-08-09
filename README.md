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
# ---------------------------------------------------------------------
# 1. FUNCTION DEFINITIONS ('def')
# ---------------------------------------------------------------------
def add(x, y):
    return x + y  # Adds the two numbers together

def subtract(x, y):
    return x - y  # Subtracts y from x

def multiply(x, y):
    return x * y  # Multiplies the two numbers

def divide(x, y):
    if y == 0:
        return "Error: Cannot divide by zero!"
    return x / y  # Divides x by y


# ---------------------------------------------------------------------
# 2. MAIN PROGRAM LOOP ('while')
# ---------------------------------------------------------------------
while True:
    print("\n--- Termux Python Calculator ---")
    print("Enter '+', '-', '*', '/' or 'exit' to quit.")
    
    # input() captures what you type, and .strip() cleans off accidental spaces
    operator = input("Choose an operation: ").strip()
    
    # -----------------------------------------------------------------
    # 3. CONDITIONAL LOGIC ('if', 'elif')
    # -----------------------------------------------------------------
    if operator.lower() == 'exit':
        print("Goodbye!")
        break  # Stops the infinite loop entirely
        
    if operator not in ['+', '-', '*', '/']:
        print("Invalid operator! Please try again.")
        continue  # Restarts the loop back from the top

    # -----------------------------------------------------------------
    # 4. ERROR HANDLING ('try', 'except')
    # -----------------------------------------------------------------
    try:
        # float() turns text strings into real mathematical decimal numbers
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))
    except ValueError:
        print("Invalid input! Please enter numbers only.")
        continue  # Safely restarts the loop instead of crashing

    # -----------------------------------------------------------------
    # 5. ROUTING LOGIC & EXECUTION
    # -----------------------------------------------------------------
    if operator == '+':
        result = add(num1, num2)
    elif operator == '-':
        result = subtract(num1, num2)
    elif operator == '*':
        result = multiply(num1, num2)
    elif operator == '/':
        result = divide(num1, num2)
    
    # Displays the final math answer on your Termux screen
    print(f"Result: {result}")
```</code></pre>

<FollowUp>
Once you **paste this and click commit**, check out your main repository page. Does the calculator guide show up nicely inside its dark code container now?
</FollowUp>
