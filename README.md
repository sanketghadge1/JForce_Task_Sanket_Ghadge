# JForce Solutions – SQL Developer Stored Procedure Task

## Project Overview

This project demonstrates MySQL Stored Procedures for an Employee Management and Payroll database.

The solution covers:

* Stored procedure creation
* IN parameters
* Conditional logic using IF/ELSEIF/ELSE
* CASE expressions
* Salary calculations
* Aggregate functions
* Input validation
* Basic error handling

## Database

Database name:

`employee_payroll`

## Table

The project contains an `employees` table with the following columns:

* `employee_id`
* `employee_name`
* `department`
* `designation`
* `basic_salary`
* `joining_date`
* `status`

The database contains 10 sample employees from different departments and salary ranges.

## Stored Procedures

### 1. GetEmployeeSalaryReport

Returns active employees from a specified department whose salary is greater than or equal to the specified minimum salary.

Example:

```sql
CALL GetEmployeeSalaryReport('IT', 50000);
```

### 2. CalculateEmployeeSalary

Calculates:

* HRA = 20% of Basic Salary
* DA = 10% of Basic Salary
* PF = 12% of Basic Salary
* Net Salary = Basic Salary + HRA + DA - PF

Example:

```sql
CALL CalculateEmployeeSalary(101);
```

### 3. EmployeeSalaryGrade

Assigns a salary grade according to basic salary:

* Below ₹30,000 → C
* ₹30,000–₹60,000 → B
* Above ₹60,000 → A

Example:

```sql
CALL EmployeeSalaryGrade(101);
```

### 4. GetDepartmentSummary

Returns department-level salary information:

* Total employees
* Average salary
* Highest salary
* Lowest salary
* Total salary expenditure

Example:

```sql
CALL GetDepartmentSummary('IT');
```

The procedure also validates whether the requested department exists.

## How to Run

### Step 1

Run `database.sql` to create the database, table, and sample data.

### Step 2

Run `procedures.sql` to create all stored procedures.

### Step 3

Execute the procedures using the sample `CALL` statements.

## Technologies

* MySQL
* SQL
* Stored Procedures
* Aggregate Functions
* Conditional Logic

