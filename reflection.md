# Lab 5 — Static Code Analysis

**Student Name:** Pruthviraj Ajay Patil  
**SRN:** PES1UG24CS345  
**Assigned Repository:** L5_37_todo_manager

## Reflection Questions and Answers

### 1. What is static code analysis?

Static code analysis is the process of examining source code without executing the program. It helps identify potential programming errors, security vulnerabilities, and coding-style violations.

### 2. What is the difference between Pylint, Bandit, and Flake8?

Pylint identifies code-quality issues, possible programming mistakes, and naming problems. Bandit focuses on common security vulnerabilities in Python code. Flake8 checks coding style, formatting, and adherence to Python conventions.

### 3. What issues were identified and fixed during the lab?

The code review identified potentially unsafe pickle deserialization, shell-command construction, a mutable default argument, inconsistent function naming, missing explicit return behavior, missing file encoding, empty-list handling, and unconditional execution of the demonstration. Fixes were applied to improve security, reliability, and maintainability.

### 4. What did you learn from this lab?

I learned that static analysis tools can identify potential problems before program execution. Using Pylint, Bandit, and Flake8 together provides broader coverage of code quality, security, and formatting. However, static analysis should also be supported by runtime testing and verification of the reported findings.