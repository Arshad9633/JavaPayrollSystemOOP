# Employee Payroll System

A simple Java application demonstrating Object-Oriented Programming (OOP) concepts like abstraction, inheritance, polymorphism, and encapsulation. The system manages full-time and part-time employees, calculates their salaries, and provides functionalities to add, remove, and display employees.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Classes](#classes)
- [Usage](#usage)

## Introduction

The Employee Payroll System is a Java application designed to manage employees and calculate their salaries. 
It uses OOP principles to create a flexible and maintainable codebase. The system supports both full-time 
and part-time employees.

## Features

- Add new employees (full-time and part-time)
- Remove employees by ID
- Display employee details
- Calculate salaries for both full-time and part-time employees

## Classes

### Employee (abstract class)

- **Attributes**: `name`, `id`
- **Methods**: `getName()`, `getId()`, `calculateSalary()`, `toString()`

### FullTimeEmployee (extends Employee)

- **Attributes**: `monthlySalary`
- **Methods**: `calculateSalary()`

### PartTimeEmployee (extends Employee)

- **Attributes**: `hoursWorked`, `hourlyRate`
- **Methods**: `calculateSalary()`

### PayrollSystem

- **Attributes**: `employeeList` (ArrayList of Employee)
- **Methods**: `addEmployee(Employee employee)`, `removeEmployee(int id)`, `displayEmployees()`

## Usage

### Adding an Employee

To add a new employee, create an instance of either `FullTimeEmployee` or `PartTimeEmployee` and add it to the `PayrollSystem`:

```java
PayrollSystem payrollSystem = new PayrollSystem();
FullTimeEmployee emp1 = new FullTimeEmployee("John Doe", 1, 5000);
PartTimeEmployee emp2 = new PartTimeEmployee("Jane Smith", 2, 20, 25);

payrollSystem.addEmployee(emp1);
payrollSystem.addEmployee(emp2);
