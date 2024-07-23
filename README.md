# SQL-DATABASE

## Employee DBMS

### Setup
To set up the database, execute the following SQL script to create the employees table:

```sql
CREATE TABLE employees (
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(400),
    role VARCHAR(200),
    salary INT
    age INT,
    address VARCHAR(350),
    phone VARCHAR(200)
);
```

### Add Multiple Employees with Selective Data

```sql
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Meshva', 'CEO', 100000, 20, 'Surat', '9313220217');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Mahi', 'HR', 80000, 25, 'Pune', '9099412865');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Dipali', 'Accountant', 50000, 25, 'Vasad', '9904682617');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Drashti', 'Manager', 95000, 22, 'Vapi', '7046615707');
INSERT INTO employees (name, role, salary, age, address, phone) VALUES ('Anjali', 'PRO', 70000, 18, 'Surat', '7096612450');
```

### Retrieve All Employee Information
```sql
SELECT * FROM employees;
```

### Find Employees with a Specific Role
```sql
SELECT * FROM employees WHERE role = 'Manager';
```

### Search for Employees with Names Containing "Me"
```sql
SELECT * FROM employees WHERE LOWER(name) LIKE '%Me%';
```

### Find Employees Older than 30 and Earning More than $70,000
```sql
SELECT * FROM employees WHERE age > 30 AND salary > 70000;
```

### Change the Salary of an Employee with ID 3
```sql
UPDATE employees SET salary = 30000 WHERE id = 3;
```

### Update the Address for Employees in the 'Maneger' Role
```sql
UPDATE employees SET address = 'Pune' WHERE role = 'Maneger';
```

### Remove an Employee with ID 4
```sql
DELETE FROM employees WHERE id = 4;
```

## Delete All Employees with Age Less than 20
```sql
DELETE FROM employees WHERE age < 20;
```
