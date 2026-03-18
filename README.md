# Function Call Order Parser in C (Using Stacks)

## 📌 Objective
Design and implement a C program that parses another C source file and verifies whether the function call sequence follows a valid order using a stack-based approach.

---

## 📖 Problem Description

Write a **C parser program** that reads a C source file with the following constraints:

1. The source file contains `stdio.h` as its header.
2. It defines functions named:
f1(), f2(), f3(), ..., fn() where 1 ≤ n ≤ 9
3. The `main()` function always begins execution by calling `f1()`.
4. Functions may:
- Call each other in any order.
- Have any number of arguments.
- Return any primitive data type (`int`, `float`, `char`, etc.).
5. Function calls may be nested.

---

## ⚙️ Task Requirements

### 1. File Parsing
- Read and scan the entire C source file.
- Identify all function definitions and function calls.

### 2. Stack Implementation
- Use a stack data structure to track function calls.
- Push a function onto the stack when it is called.
- Pop it when the function execution completes (simulate call-return behavior).

### 3. Validation Logic
Ensure that:
- Execution starts from `main()` and the first call is `f1()`.
- Every function call follows a valid stack-based call-return sequence.

Detect and report:
- Invalid function calls  
- Incorrect return order  
- Missing or extra function returns  

### 4. Output
- If the function call order is correct, print:

  Valid function call sequence.

- Otherwise, print:

   Invalid function call sequence.
