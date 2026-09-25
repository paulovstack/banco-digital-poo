# DevBank

A simple banking system built in Python, simulating the operations of a digital banking application: the user registers an account and can make deposits and withdrawals based on the available account balance.

## Features

* Initial account holder registration
* Balance inquiry
* Depositing funds
* Withdrawing funds (with sufficient balance verification)
* Interactive terminal menu with visual feedback (colored messages and loading simulation)

## Concepts Practiced

This project was my way of practicing **Object-Oriented Programming (OOP)** in Python, mainly:

* **Inheritance**: the `Conta` class inherits from `Depositar` and `Sacar`, which in turn inherit from `ContaBancaria`. This avoids code duplication, since each specialized class only implements the behavior specific to it.
* **Encapsulation**: the account attributes (`_titular`, `_saldo`) are protected (using the `_` prefix), indicating that they should not be directly modified from outside the class, but rather through defined methods such as `depositar` and `sacar`.
* Control structures (`while`, `if/elif/else`) for the menu and the logic of each operation.
* Terminal output formatting, including colors (ANSI escape codes) to improve the user experience.

## How to Run

```bash
python main.py
```

The program will ask for your name and CPF (simulated; the format is not actually validated), create your account with an initial balance of zero, and open the menu with options for deposits, withdrawals, and exiting the program.

## Technologies

* Python 3
* Standard libraries: `time`, `os`

## Future Improvements

* Data persistence (save the account to a file so the balance is not lost when the program is closed)
* Real CPF validation
* Transaction history
