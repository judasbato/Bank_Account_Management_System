# Bank Account Management System

## Table of Contents
1. [Description](#description)
2. [Features](#features)
3. [Files](#files)
4. [Getting Started](#getting-started)
5. [Usage](#usage)
6. [Code Highlights](#code-highlights)
7. [Example Output](#example-output)
8. [Acknowledgements](#acknowledgements)

## Description
This project is a simple C++ implementation of a bank account management system. The program includes several types of accounts, each with specific deposit and withdrawal rules. It demonstrates object-oriented programming concepts such as inheritance, polymorphism, and operator overloading.

## Features
The program supports the following account types:
- **Account**: A basic account with standard deposit and withdrawal functionalities.
- **Checking Account**: Inherits from `Account` and charges a fee for each withdrawal.
- **Savings Account**: Inherits from `Account` and offers interest on deposits.
- **Trust Account**: Inherits from `Savings Account` and includes additional restrictions on withdrawals, as well as bonuses for large deposits.

## Files
- `Account.h` / `Account.cpp`: Base class defining the common properties and methods for accounts.
- `Savings_Account.h` / `Savings_Account.cpp`: Derived class for savings accounts, adding interest rate functionality.
- `Checking_Account.h` / `Checking_Account.cpp`: Derived class for checking accounts, applying a withdrawal fee.
- `Trust_Account.h` / `Trust_Account.cpp`: Derived class for trust accounts, adding withdrawal limits and a bonus system.
- `Account_Util.h` / `Account_Util.cpp`: Helper functions for displaying, depositing, and withdrawing from collections of accounts.
- `main.cpp`: Main program that creates account instances, deposits, and withdraws funds while displaying results.

## Getting Started
### Prerequisites
- C++ compiler (e.g., GCC, Clang)
- Basic knowledge of C++ and object-oriented programming

### Building and Running
1. Clone the repository or download the source files.
2. Compile the code using a C++ compiler. For example:
    ```bash
    g++ main.cpp Account.cpp Checking_Account.cpp Savings_Account.cpp Trust_Account.cpp Account_Util.cpp -o bank_system
    ```
3. Run the compiled executable:
    ```bash
    ./bank_system
    ```

## Usage
The main program (`main.cpp`) demonstrates how to:
1. Create instances of different account types.
2. Display account information.
3. Deposit and withdraw funds from accounts.
4. Use utility functions to handle multiple accounts.

Sample code to create and manage accounts:
```cpp
#include "Account.h"
#include "Savings_Account.h"
#include "Checking_Account.h"
#include "Trust_Account.h"
#include "Account_Util.h"

int main() {
    std::vector<Account> accounts;
    accounts.push_back(Account("Basic Account", 1000.0));
    display(accounts);
    deposit(accounts, 200.0);
    withdraw(accounts, 50.0);
}
```
## Code Highlights
- **Inheritance**: Each account type inherits from a base `Account` class and extends its functionality.
- **Operator Overloading**: The `<<` operator is overloaded to print account information.
- **Polymorphism**: The system is designed to operate on collections of accounts with different types.

## Example Output
```css
=== Accounts ============================================
[Account: Basic Account: 1000.00]

=== Depositing to Accounts =================================
Deposited 200.00 to [Account: Basic Account: 1200.00]

=== Withdrawing from Accounts ==============================
Withdrew 50.00 from [Account: Basic Account: 1150.00]
```

## Acknowledgements
Inspired by basic concepts in object-oriented programming and C++ for learning purposes.
