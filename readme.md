# Project: Calculator with GUI

This is a simple calculator with a GUI
> **Goal:** GUI, calculations and call functions in order

## Task

Create a Calculator

### Input

* GUI input
  * numbers
  * operations
    * Addition (+)
    * Substraction (-)
    * Multiplication (*)
    * Division (/)
    * Exponentiation
      * potentiation (**)
      * square root (sqrt())
      * qubic root (**(1./3.))
      * x root (**(1./x.))
  * minus sign (-)
  * float point
  * compute (=)

### Conversions

* check if calculation is possible (division by 0)
* calculate

### Output

* result
* Feedback when division is not possible

## Psuedo code

```text
TipCalculator
    Initialize calculator
    Initilaize GUI

    Prompt for equation

    Convert numbers to numbers (float)
    Calculate operations in order while checking if operations are possible
    
    Feedback-Pop-Up on error if error
    Display result or 
End

```

## Project Structure

```text
.
├── .gitignore
├── readme.md
├── requirements.txt
├── calculator
│   ├── __init__.py
│   └── calculator.py
├── simple_gui
│   ├── __init__.py
│   └── simple_gui.py
└── tests/
    ├── __init__.py
    └── test_calculator.py
```

## Tests

* Operations (as float)
  * Addition (+)
  * Substraction (-)
  * Multiplication (*)
  * Division (/)
  * Exponentiation
    * potentiation (**)
    * square root (sqrt())
    * qubic root (**(1./3.))
    * x root (**(1./x.))
* Division by 0
* Operations hirarchy (PEMDAS[^1])
  * Parentheses, Exponents, Multiplication/Division, Addition/Subtraction from left to right.

### Assertion-Test: Operations (as float)

**Test-Plan: Addition (+)**

```text
Inputs:
  123.45 + 670.89
Expected result:
  794.34
```

**Test-Plan: Substraction (-)**

```text
Inputs:
  670.89 - 123.45
Expected result:
  547.44
```

**Test-Plan: Multiplication (*)**

```text
Inputs:
    123.45 * 670.89
Expected result:
  82821.3705
```

**Test-Plan: Division (/)**

```text
Inputs:
  123.45 / 670.89
Expected result:
  0,1840093010776729
```

**Test-Plan: Exponentiation, potentiate (\*\*)**

```text
Inputs:
  123.4567809 ** 2
  123.4567809 ** 3
  123.4567809 ** 4
  123.4567809 ** 5
  123.4567809 ** 6
  123.4567809 ** 7
  123.4567809 ** 8
  123.4567809 ** 9
Expected result:
  15241.576750190605
  1881676.0014188155
  232305661.83195078
  28679709194.616642
  3540704574315.502
  437123988862896.7
  5.396592051918067e+16
  6.662458825603302e+18
```

**Test-Plan: Exponentiation, square root (sqrt())**

```text
Inputs:
  123.4567809 ** (1/2)
Expected result:
  11.111110696055547
```

**Test-Plan: Exponentiation, qubic root (\*\*(1./3.))**

```text
Inputs:
  123.4567809 ** (1/3)
Expected result:
  4.979338483283606
```

**Test-Plan: Exponentiation, x root (\*\*(1./x.))**

```text
Inputs:
  123.4567809 ** (1/4)
  123.4567809 ** (1/5)
  123.4567809 ** (1/6)
  123.4567809 ** (1/7)
  123.4567809 ** (1/8)
  123.4567809 ** (1/9)
Expected result:
  3.333333271074998
  2.620010246173881
  2.2314431391553775
  1.9897011447521342
  1.8257418413004063
  1.7076173150528808

```

### Assertion-Test: Division by 0

**Test-Plan:**

```text
Inputs:
  10 / 0 
Expected result:
  ZeroDivisionError
```

### Assertion-Test: Operations hirarchy (PEMDAS)

**Test-Plan:**

```text
Inputs:
  10 + 15 * (3 - 8) ** 5
Expected result:
  -46885
```

## Additional, optional Tasks

* Add brackets/paranthethes functionality
* Add scientific calculations
* Display thousand-sepeartor on input "1,000,000.00"

[^1]: [Order of operations](https://en.wikipedia.org/wiki/Order_of_operations) from *Ali Rahman, Ernna Sukinnah; Shahrill, Masitah; Abbas, Nor Arifahwati*; Tan, Abby (Summer 2017) [2016-08-29, 2017-03-06]. "Developing Students' Mathematical Skills Involving Order of Operations" ([:link: PDF](https://files.eric.ed.gov/fulltext/EJ1148460.pdf)). *International Journal of Research in Education and Science (IJRES)*. University of Brunei Darussalam. 3 (2): 373–382. [doi:10.21890/ijres.327896](https://doi.org/10.21890%2Fijres.327896). [ISSN 2148-9955](https://www.worldcat.org/issn/2148-9955).