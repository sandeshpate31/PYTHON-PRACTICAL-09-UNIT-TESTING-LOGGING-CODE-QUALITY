# Python Practical 09 – Unit Testing, Logging and Code Quality

## Student Practical

**NAME** **:-** SANDESH PATE,
**ROLL NO** **:-**  25,

The practical covers:

1. Unit Testing using `pytest`.
2. Testing valid and invalid inputs.
3. Handling expected exceptions using `pytest.raises()`.
4. Python Logging using DEBUG, INFO, WARNING, ERROR and CRITICAL levels.
5. Code quality checking using Ruff.
6. Automatic code formatting using Ruff.

---

## Project Objectives

- Understand how to write unit tests for Python functions.
- Identify errors using automated testing.
- Record application activities using Python logging.
- Understand different logging levels.
- Identify unused imports and variables using Ruff.
- Format Python code according to consistent coding standards.

---

## Project Structure

```text
Python_Practical-09/
│
├── order.py
│
├── test_order.py
│
├── logging_demo.py
│
├── bad_code.py
│
├── requirements.txt
│
├── README.md
│
├── .gitignore
│
├── Screenshots/
│   └── pratical-10(1).png
│
└── .venv/                 # Virtual environment (not uploaded)
```

---

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| pytest | Unit testing |
| Logging | Application event and error recording |
| Ruff | Code quality checking |
| VS Code | Development environment |

**Requirements:**
- Python 3.10 or newer
- pip
- Visual Studio Code

---

# Part A – Unit Testing with pytest

## 1. Order Processing System

The `order.py` file contains the business logic for calculating order discounts, GST and final order amounts.

### Functions Implemented

| Function | Description |
|---|---|
| `calculate_discount()` | Calculates discount amount |
| `calculate_gst()` | Calculates GST amount |
| `calculate_order_total()` | Calculates final order amount after discount and GST |

### Example Calculation

Order Price = ₹1,000

Discount = 10%

GST = 18%

Calculation:

1. Discount = ₹1,000 × 10% = ₹100
2. Discounted Price = ₹1,000 − ₹100 = ₹900
3. GST = ₹900 × 18% = ₹162
4. Final Order Amount = ₹900 + ₹162 = ₹1,062

### Execute Order Processing System

```powershell
python order.py
```

Expected Output:

```text
Final order amount: ₹1062.00
```

---

## 2. Unit Testing using pytest

The `test_order.py` file contains automated test cases for the order calculation functions.

### Test Cases

- Calculate discount.
- Calculate GST.
- Calculate order total.
- Check zero discount.
- Reject negative price.
- Reject invalid discount.
- Reject invalid GST rate (if included in the test file).

### Run All Unit Tests

```powershell
python -m pytest -v
```

### Important pytest Commands

Run only order tests:

```powershell
python -m pytest -v test_order.py
```

Check pytest version:

```powershell
python -m pytest --version
```

### Testing Concepts

- **assert:** Checks whether the actual result matches the expected result.
- **pytest.raises():** Verifies that the expected exception is raised.
- **Test Case:** An individual test of a particular function or condition.
- **Test Suite:** A collection of related test cases.
- **Regression Testing:** Re-running tests after code changes to check existing functionality.

---

# Part B – Logging in Python

## 3. Python Logging Demonstration

The `logging_demo.py` file demonstrates Python's built-in logging module.

Logging records application events, warnings and errors during program execution.

### Logging Levels

| Level | Description |
|---|---|
| DEBUG | Detailed debugging information |
| INFO | Normal application events |
| WARNING | Unexpected situations |
| ERROR | Errors during application execution |
| CRITICAL | Serious application failures |

### Logging Configuration

The application uses:

- `filename="application.log"` – Stores logs in a file.
- `level=logging.DEBUG` – Enables all five logging levels.
- `format` – Displays timestamps, severity levels and messages.
- `logging.getLogger(__name__)` – Creates a module-specific logger.

### Execute Logging Demonstration

```powershell
python logging_demo.py
```

A file named `application.log` is generated in the project folder.

Open the log file:

```powershell
notepad application.log
```

The log file contains application events with timestamps and severity levels.

---

# Part C – Code Quality with Ruff

## 4. Ruff Installation

Ruff is a Python linting and formatting tool used to identify common code-quality issues.

Install Ruff:

```powershell
python -m pip install ruff
```

Check the installed version:

```powershell
python -m ruff --version
```

## 5. Ruff Code Quality Demonstration

The `bad_code.py` file contains intentionally untidy Python code to demonstrate code-quality checking.

### Check Code Quality

```powershell
python -m ruff check bad_code.py
```

### Apply Automatic Fixes

```powershell
python -m ruff check bad_code.py --fix
```

If Ruff reports an unsafe fix, review the suggested change and apply it manually when appropriate.

### Format Python Code

```powershell
python -m ruff format bad_code.py
```

### Check All Python Files

```powershell
python -m ruff check .
```

### Verify Code Formatting

```powershell
python -m ruff format --check .
```

### Common Code Quality Issues

- Unused imports.
- Unused variables.
- Inconsistent formatting.
- Improper spacing.
- Code readability issues.

---

# Installation and Setup

## 6. Create Virtual Environment

Open PowerShell inside the project directory.

Create the virtual environment:

```powershell
python -m venv .venv
```

Activate it:

```powershell
.venv\Scripts\Activate.ps1
```

If PowerShell blocks activation, execute:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
```

Then activate again:

```powershell
.venv\Scripts\Activate.ps1
```

## 7. Install Required Libraries

Upgrade pip:

```powershell
python -m pip install --upgrade pip
```

Install pytest and Ruff:

```powershell
python -m pip install pytest ruff
```

---

# Complete Practical Execution

Run the following commands in order:

### 1. Execute Order Processing

```powershell
python order.py
```

### 2. Execute Unit Tests

```powershell
python -m pytest -v
```

### 3. Execute Logging

```powershell
python logging_demo.py
```

### 4. Open Application Log

```powershell
notepad application.log
```

### 5. Check Code Quality

```powershell
python -m ruff check bad_code.py
```

### 6. Apply Ruff Fixes

```powershell
python -m ruff check bad_code.py --fix
```

### 7. Format Code

```powershell
python -m ruff format bad_code.py
```

### 8. Final Code Quality Check

```powershell
python -m ruff check .
```

```powershell
python -m ruff format --check .
```

---

# Screenshots and Practical Output

The following screenshots show the execution and output of Python Practical 09.

### Screenshot 1 – Practical Execution

![Practical 09 Screenshot 1](Screenshots/pratical-10(1).png)

**Image Path:**
`Screenshots\pratical-10(1).png`

### Screenshot 2 – Practical Execution

![Practical 09 Screenshot 2](Screenshots/pratical-10(2).png)

**Image Path:**
`Screenshots\pratical-10(2).png`

### Screenshot 3 – Practical Execution

![Practical 09 Screenshot 3](Screenshots/pratical-10(3).png)

**Image Path:**
`Screenshots\pratical-10(3).png`

### Screenshot 4 – Practical Execution

![Practical 09 Screenshot 4](Screenshots/pratical-10(4).png)

**Image Path:**
`Screenshots\pratical-10(4).png`

### Screenshot 5 – Practical Execution

![Practical 09 Screenshot 5](Screenshots/pratical-10(5).png)

**Image Path:**
`Screenshots\pratical-10(5).png`

### Screenshot 6 – Practical Execution

![Practical 09 Screenshot 6](Screenshots/pratical-10(6).png)

**Image Path:**
`Screenshots\pratical-10(6).png`

### Screenshot 7 – Practical Execution

![Practical 09 Screenshot 7](Screenshots/pratical-10(7).png)

**Image Path:**
`Screenshots\pratical-10(7).png`

### Screenshot 8 – Practical Execution

![Practical 09 Screenshot 8](Screenshots/pratical-10(8).png)

**Image Path:**
`Screenshots\pratical-10(8).png`

### Screenshot 9 – Practical Execution

![Practical 09 Screenshot 9](Screenshots/pratical-10(9).png)

**Image Path:**
`Screenshots\pratical-10(9).png`




---

**Note:** All screenshots are stored inside the `Screenshots` folder of the project. Ensure that all 10 image files are present before pushing the project to GitHub.

---

# GitHub Repository Upload

## Suggested Repository Name

`PYTHON-PRACTICAL-09-UNIT-TESTING-LOGGING-CODE-QUALITY`

## Repository Description

Python Practical 09 – Implementation of Unit Testing using pytest, Python Logging and Code Quality checking using Ruff. Includes an Order Processing System with discount calculation, GST calculation, automated test cases, application logging and code formatting.

## Git Commands

Initialize Git:

```powershell
git init
```

Add project files:

```powershell
git add .
```

Check files before committing:

```powershell
git status
```

Commit changes:

```powershell
git commit -m "Complete Python Practical 09"
```

Rename the branch:

```powershell
git branch -M main
```

Connect GitHub repository:

```powershell
git remote add origin https://github.com/sandeshpate31/PYTHON-PRACTICAL-09-UNIT-TESTING-LOGGING-CODE-QUALITY.git
```

Push project to GitHub:

```powershell
git push -u origin main
```

**Note:** Replace the repository URL if you create a repository with a different name.

Do not upload the `.venv` folder, Python cache folders or generated `application.log` file. These files should be excluded using `.gitignore`.

---

# Conclusion

This practical demonstrates the importance of unit testing, logging and code quality in Python application development.

The Order Processing System demonstrates discount calculation, GST calculation and final order amount calculation.

pytest is used to verify application functionality, Python logging records application events and errors, and Ruff identifies common code-quality issues and formats Python code.

These techniques help developers create readable, reliable and maintainable applications.