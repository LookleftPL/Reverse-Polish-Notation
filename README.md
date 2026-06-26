# Reverse Polish Notation (RPN) Converter and Evaluator

Project focuses on implementing the Shunting-yard algorithm and an RPN evaluation mechanism from scratch in C++. The program provides a text-based interface allowing users to convert standard infix mathematical expressions into Reverse Polish Notation (Postfix) and calculate their numerical results, handling operator precedence and associativity without external parsing libraries.

## Features

### 1. Infix to Postfix Conversion (Shunting-yard Algorithm)
* Parsing of mathematical expressions where tokens (numbers, operators) are separated by spaces.
* Fully customized operator precedence routing:
  * Unary operators / Special tokens (Priority 4)
  * Power operator `^` (Priority 3)
  * Multiplication `*` and Division `/` (Priority 2)
  * Addition `+` and Subtraction `-` (Priority 1)
* Robust handling of parentheses `()` to dynamically alter calculation order during the stack-shifting process.

### 2. RPN Expression Evaluation
* Postfix notation processing using a dedicated data stack for operands.
* Multi-operation support for standard arithmetic operations including addition, subtraction, multiplication, division, and exponentiation (`pow`).

## Complexity Analysis

### Infix to Postfix Conversion
* **Time Complexity**: O(n) — The algorithm processes each token from the input expression exactly once. Push and pop operations on the stack run in O(1) time. Nested loops do not increase the complexity beyond linear, as each operator enters and leaves the stack at most once.
* **Space Complexity**: O(n) — Memory allocation scales linearly based on the number of tokens stored within the auxiliary stack and the final output collection.

### RPN Evaluation
* **Time Complexity**: O(n) — The application loops through the processed RPN token collection exactly once, performing constant-time arithmetic execution for each step.
* **Space Complexity**: O(n) — In the worst-case scenario, the operand stack holds a fraction of the total token count proportional to the size of the expression input.

## Getting Started

### Prerequisites
* A C++ compiler supporting C++11 or higher.

### Compilation and Execution
To compile the project using GCC via the command line, navigate to the project directory and run:

```bash
g++ main.cpp -o program
