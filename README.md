# DA5301W: Python for Data Science

Welcome to the course repository for **DA5301W – Python for Data Science**.
This README explains how to set up your workspace and describes **Assignment 0**.

---

## Table of Contents

1. [Prerequisites](#1-prerequisites)
2. [Getting Started](#2-getting-started)
   - [Clone the repository](#21-clone-the-repository)
   - [Add the cloned folder to `.gitignore`](#22-add-the-cloned-folder-to-gitignore)
   - [Create a folder for Assignment 0](#23-create-a-folder-for-assignment-0)
3. [Assignment 0: Leap Year Calculator](#3-assignment-0-leap-year-calculator)
4. [Submission Guidelines](#4-submission-guidelines)

---

## 1. Prerequisites

Make sure you have the following installed before you begin:

| Tool | Purpose | Check with |
|------|---------|------------|
| Git | Version control | `git --version` |
| Python 3.9+ | Running your code | `python --version` |
| Jupyter Notebook / JupyterLab / VS Code (with the Jupyter extension) | Working with `.ipynb` files | `jupyter --version` |

You also need a GitHub account.

---

## 2. Getting Started

### 2.1 Clone the repository

Open a terminal (Git Bash on Windows) and navigate to the place where you keep your coursework:

```bash
cd path/to/your/workspace
```

Clone the course repository:

```bash
git clone <COURSE_REPO_URL>
```

> Replace `<COURSE_REPO_URL>` with the repository link shared by the instructor,
> e.g. `https://github.com/<org>/DA5301W.git`.

This creates a new folder (named after the repository) in your current directory.
Move into it to confirm it worked:

```bash
cd DA5301W
```

### 2.2 Add the cloned folder to `.gitignore`

The cloned course folder should **not** be tracked by your own submission repository.
In the directory that *contains* the cloned folder (your own working repo), open or create a file named `.gitignore` and add the name of the cloned folder to it.

**Using the terminal (macOS / Linux / Git Bash):**

```bash
echo "DA5301W/" >> .gitignore
```

**Or manually:** open `.gitignore` in any text editor and add this line:

```
DA5301W/
```

It is also a good idea to ignore Jupyter and Python clutter:

```
.ipynb_checkpoints/
__pycache__/
*.pyc
.venv/
```

Verify that Git now ignores the folder:

```bash
git status
```

The cloned folder should **no longer appear** in the list of untracked files.

### 2.3 Create a folder for Assignment 0

Create a separate folder for each assignment in **your own working directory**
(not inside the cloned course folder):

```bash
mkdir assignment_0
cd assignment_0
```

Your workspace should now look like this:

```
your-workspace/
├── .gitignore
├── DA5301W/              <- cloned course repo (ignored by Git)
└── assignment_0/         <- your work goes here
    └── leap_year.ipynb   <- you will create this
```

Launch Jupyter from inside `assignment_0` and create a new notebook named `leap_year.ipynb`:

```bash
jupyter notebook
```

---

## 3. Assignment 0: Leap Year Calculator

### 3.1 Problem Definition

Write a Python program, inside a Jupyter notebook (`.ipynb`), that takes a year as input and determines whether it is a **leap year**.

A year is a leap year if it satisfies the following rules:

1. It is divisible by **4**, **and**
2. It is **not** divisible by **100**, **unless**
3. It is also divisible by **400**.

In short:

```
leap year  =  (year % 4 == 0 and year % 100 != 0) or (year % 400 == 0)
```

### 3.2 Input

| Item | Description |
|------|-------------|
| `year` | A positive integer entered by the user (e.g. `2024`) |

- Read the value using `input()` and convert it to an integer.
- Your program should handle invalid input gracefully (e.g. text, decimals, zero, or negative numbers) by showing a helpful message instead of crashing.

### 3.3 Output

Print a clear message stating whether the year is a leap year:

```
2024 is a leap year.
```
```
2023 is not a leap year.
```

### 3.4 Sample Test Cases

| Input | Expected Output | Reason |
|-------|-----------------|--------|
| `2024` | Leap year | Divisible by 4, not by 100 |
| `2023` | Not a leap year | Not divisible by 4 |
| `1900` | Not a leap year | Divisible by 100 but not by 400 |
| `2000` | Leap year | Divisible by 400 |
| `2100` | Not a leap year | Divisible by 100 but not by 400 |
| `abc` | Error message | Invalid input |
| `-5` | Error message | Year must be positive |

### 3.5 Requirements

- The solution must be written in a single Jupyter notebook: `leap_year.ipynb`.
- Define a **function**, e.g. `is_leap_year(year)`, that returns `True` or `False`.
- Use the function to print the final message for user input.
- Include **input validation** as described above.
- Test your function on **all the sample cases** in the table above and show the results in the notebook.
- Add **Markdown cells** explaining the problem and your approach, and use **comments** in your code.
- Run **Kernel → Restart & Run All** before saving so that all outputs are visible.

### 3.6 Suggested Notebook Structure

1. **Title and problem statement** (Markdown)
2. **Approach / logic** (Markdown)
3. **Function definition:** `is_leap_year(year)` (Code)
4. **Taking user input with validation** (Code)
5. **Displaying the result** (Code)
6. **Test cases** (Code)

### 3.7 Learning Objectives

By completing this assignment you will practise:

- Setting up Git and cloning a repository
- Organising coursework into folders
- Working with Jupyter notebooks
- Conditionals, logical operators, and the modulus operator
- Writing reusable functions
- Basic input handling and validation

---

## 4. Submission Guidelines

1. Make sure your `assignment_0/` folder contains `leap_year.ipynb` with all outputs visible.
2. Commit your work:

   ```bash
   git add assignment_0/
   git commit -m "Add Assignment 0: leap year calculator"
   ```

3. Push to your GitHub repository:

   ```bash
   git push origin main
   ```

4. Submit the link to your repository / notebook as instructed by the course staff.

**Deadline:** `<DEADLINE_DATE>`

---

**Course:** DA5301W – Python for Data Science
**Instructor / TAs:** `<NAMES / CONTACT>`
