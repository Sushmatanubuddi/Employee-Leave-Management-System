# 🧾 Employee Leave Management System (Oracle SQL + PL/SQL)

This project is a simple **Employee Leave Management System** developed using Oracle SQL and PL/SQL. It allows for managing employee data, tracking leave balances, applying for leave, and validating leave requests.

---

## 📌 Features

- Add and maintain employee records.
- Track sick and casual leave balances.
- Employees can apply for leave.
- Leave type validation using stored procedures.
- Prevent applying for past-dated leaves using a trigger.

---

## 🛠 Technologies Used

- Oracle SQL
- PL/SQL (Stored Procedures & Triggers)
- SQL*Plus for execution

---

## 🗂 Project Structure

| File Name            | Description                                     |
|---------------------|-------------------------------------------------|
| `employee_schema.sql` | Creates tables and sequences                    |
| `sample_data.sql`     | Inserts sample employee and leave balance data |
| `procedures.sql`      | Procedure to apply for leave                   |
| `triggers.sql`        | Trigger to prevent past-date leave requests    |
| `test_cases.sql`      | Test scenarios to check functionality          |

---

## 🧪 Sample Procedure Flow

```plsql
EXEC apply_leave(
    p_emp_id => 101,
    p_leave_type => 'sick',
    p_start_date => TO_DATE('2025-05-25','YYYY-MM-DD'),
    p_end_date => TO_DATE('2025-05-26','YYYY-MM-DD')
);
