# STAFF_DEPARTMENT

## Description

This repository contains SQL code for creating two tables (`employees` and `departments`) and performing various operations on them. The `employees` table stores information about employees, including their names, department IDs, and salaries. The `departments` table stores information about different departments within the organization.

## Installation

To use the SQL code in this repository, follow the steps below:

1. Ensure that you have a PostgreSQL database server installed and running.

2. Create a new database or use an existing one where you want to execute the SQL code.

3. Connect to the database using a PostgreSQL client or command-line interface.

4. Copy and execute the SQL statements in the order provided below:

```sql
CREATE TABLE employees (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50),
  department_id INT,
  salary NUMERIC(10, 2)
);

CREATE TABLE departments (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50)
);

INSERT INTO departments (name) VALUES ('Sales'), ('Marketing'), ('Finance');

INSERT INTO employees (name, department_id, salary) VALUES
  ('John Doe', 1, 60000.00),
  ('Jane Smith', 2, 45000.00),
  ('Bob Johnson', 1, 75000.00),
  ('Sara Lee', 3, 55000.00);
```

## Usage

The SQL code provided in this repository allows you to perform various operations on the `employees` and `departments` tables. Here are some examples:

### Retrieve all records from the employees table

```sql
SELECT * FROM employees;
```

### Retrieve all records from the departments table

```sql
SELECT * FROM departments;
```

### Perform an inner join between employees and departments

```sql
SELECT employees.name AS Employee, departments.name AS Department
FROM employees
INNER JOIN departments ON employees.department_id = departments.id
WHERE departments.name = 'Sales' OR departments.name = 'Marketing';
```

## Contributing

If you are a member of the development team and would like to contribute to this repository, please follow these guidelines:

1. Fork the repository to your own GitHub account.

2. Clone the forked repository to your local machine.

3. Create a new branch for your contribution:

```shell
git checkout -b feature/your-feature-name
```

4. Make the necessary changes and additions to the codebase.

5. Test your changes thoroughly to ensure they do not introduce any errors.

6. Commit your changes with a descriptive commit message:

```shell
git commit -m "Add your commit message here"
```

7. Push your changes to your forked repository:

```shell
git push origin feature/your-feature-name
```

8. Create a pull request from your forked repository to the original repository.

9. Provide a clear and detailed description of your changes in the pull request.

10. Wait for the repository owner to review your pull request and provide feedback.

11. Make any requested changes, if applicable, and push the changes to your forked repository.

12. Once your pull request is approved, it will be merged into the main repository.

Note: Please ensure that you adhere to the coding style and conventions used in this repository. Also, be respectful and considerate when interacting with other contributors.

## License

This repository is licensed under the [MIT License](LICENSE). Feel free to use the code for personal or commercial purposes.