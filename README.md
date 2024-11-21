# SmartCalc v1.0 - Calculator Program with GUI and Function Plotting

## Overview

SmartCalc v1.0 is a fully functional calculator program designed to perform complex arithmetic calculations, evaluate mathematical expressions in infix notation, and display function graphs. Developed in C language with Qt framework for the graphical user interface (GUI), SmartCalc offers a wide range of features, including standard arithmetic operations, advanced mathematical functions, variable substitution, and graph plotting for expressions involving the variable `x`.

In addition to its core functionality, the program includes bonus modes for calculating credit and deposit profitability, designed to help users make informed financial decisions.

---

## Features

### Core Functionality
- **Expression Evaluation**: Supports arithmetic expressions with the following operations:
    - Addition, Subtraction, Multiplication, Division, Power, Modulus
    - Unary Plus, Unary Minus
- **Mathematical Functions**:
    - Cosine, Sine, Tangent, Arc Cosine, Arc Sine, Arc Tangent
    - Square Root, Natural Logarithm, Common Logarithm
- **Infix Expression Parsing**: Parses and evaluates expressions written in infix notation, including nested brackets and mathematical functions.
- **Variable Substitution**: Allows the substitution of the variable `x` in the expression with a number to calculate the result.
- **Floating Point and Integer Support**: Handles both integers and real numbers with a precision of at least 7 decimal places.
- **Expression Length**: Users can input expressions up to 255 characters in length.

### Graph Plotting
- **Function Graphing**: Plots the graph of a function given in infix notation involving the variable `x`.
- **Coordinate Axes**: Displays coordinate axes with marked scales.
- **Adaptive Grid**: Automatically adjusts the grid depending on the domain and range of the plotted function.
- **Domain and Range**: Users can specify the domain and codomain of the function, limited to numbers between -1,000,000 and 1,000,000.

### Bonus Features
1. **Credit Calculator**:
    - **Inputs**: Total credit amount, term, interest rate, and type (annuity or differentiated).
    - **Outputs**: Monthly payment, overpayment on credit, and total payment.

2. **Deposit Calculator**:
    - **Inputs**: Deposit amount, term, interest rate, tax rate, payment periodicity, interest capitalization, and lists for replenishments and partial withdrawals.
    - **Outputs**: Accrued interest, tax amount, and final deposit amount at the end of the term.


---

## Requirements

### System Requirements
- **Operating System**: Linux or macOS
- **Qt Framework**: Used for GUI development
- **C Compiler**: GCC (C11 standard)

### Dependencies
- **Qt Libraries**: For graphical user interface
- **Check Library**: For unit testing modules related to expression calculation

---

## Installation

1. Clone the repository:
```bash
git clone https://github.com/le0ruslan/smart-calc.git
```

2. Navigate to the `src` directory:
```bash
cd smart-calc/src
```
3. Build the project using `Makefile`:
```bash
make
```

4. (Optional) Install the program:
```bash
   make install
```
5. To clean up the build files, run:
```bash
make clean
```

---

## Usage

1. **Basic Calculator**:
- Launch the program and enter a mathematical expression in infix notation (e.g., `(2 + 3) * 5`).
- Press the `=` button to evaluate the expression and display the result.

2. **Graph Plotting**:
- Enter an expression involving the variable `x` (e.g., `sin(x) + cos(x)`).
- Specify the domain and range for the graph.
- The program will plot the graph with coordinate axes and adaptive grid.

3. **Bonus Mode - Credit Calculator**:
- Select the "Credit Calculator" mode.
- Input the required parameters: total amount, interest rate, term, and credit type (annuity or differentiated).
- The program will output the monthly payment, overpayment, and total payment.

4. **Bonus Mode - Deposit Calculator**:
- Select the "Deposit Calculator" mode.
- Input the required parameters: deposit amount, term, interest rate, tax rate, payment periodicity, interest capitalization, and lists of replenishments and withdrawals.
- The program will output the accrued interest, tax amount, and final deposit value.

---

## Testing

Unit tests are provided for the modules related to expression calculation.
### To run the tests, execute:
```bash
make test
```
### For coverage reports, run:
```bash
make gcov_report
```
---

## Makefile Targets

The project includes a standard set of targets for building and managing the program:

- `all`: Builds the program.
- `install`: Installs the program.
- `uninstall`: Uninstalls the program.
- `clean`: Cleans up build files.
- `dvi`: Generates DVI documentation (if applicable).
- `dist`: Creates distribution files.
- `test`: Runs unit tests.
- `gcov_report`: Generates a coverage report.
