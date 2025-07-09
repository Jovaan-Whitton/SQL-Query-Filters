#  SQL Query Filters


##  Project Overview

As a security analyst at a large organization, I used SQL filtering techniques to investigate login activity and department-based machine updates across the company. This project simulates real-world incident response scenarios and showcases how SQL can be used to support enterprise security operations by isolating and analyzing data with precision.

---

## Objectives

- Apply SQL filters to large datasets
- Investigate suspicious login attempts and employee activity
- Use logical operators (WHERE, AND, OR, LIKE, NOT) for incident-driven queries
- Support security decision-making with data analysis

--- 

## Tools and Technologies

- Platform: SQL database sandbox
- Language: Structured Query Language (SQL)
- Environment: Simulated enterprise login and employee datasets

---

## Retrieve after hours failed login attempts

Investigated login attempts after business hours (18:00) to identify potential intrusions:

- `SELECT * FROM log_in_attempts
WHERE login_time > '18:00' AND success = 0;`

<details>
  <summary>Retrieve after hours login</summary>
  
![Retrieve after hours failed login attempts](images/after-hours-failures.png)

</details>

---

## Retrieve login attempts on specific dates

Queried login attempts that occurred on May 8 and May 9, 2022, to investigate a reported security event:

- `SELECT * FROM log_in_attempts
WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';`

<details>
  <summary>Retrieve login attempts on specific dates</summary>

![Retrieve login attempts on specific dates](images/login-attempts-specific-dates.png)

</details>

---

## Retrieve login attempts outside of Mexico

Filtered out all login attempts originating from Mexico to focus on international anomalies:

- `SELECT * FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';`

<details>
  <summary>Retrieve login attempts outside of mexico</summary>

![Retrieve login attempts outside of Mexico](images/outside-mexico.png)

</details>

---

## Retrieve employees in Marketing

Queried employees in the Marketing department located in the East building for targeted system updates:

- `SELECT * FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';`

<details>
  <summary>Retrieve employees in Marketing</summary>

![Retrieve employees in Marketing](images/marketing-east.png)

</details>

---

## Retrieve employees in Finance or Sales

Focused on employees in Sales or Finance departments for a scheduled policy rollout:

- `SELECT * FROM employees
WHERE department = 'Sales' OR department = 'Finance';`

<details>
  <summary>Retrieve employees in Finance or Sales</summary>

![Retrieve employees in Finance or Sales](images/sales-finance.png)

</details>

---

## Retrieve all employees not in IT

Queried all employees excluding those in Information Technology (already updated):

- `SELECT * FROM employees
WHERE NOT department = 'Information Technology';`

<details>
  <summary>Retrieve all employees not in IT</summary>

![Retrieve all employees not in IT](images/not-it.png)

</details>

---

## Summary

This project highlights my ability to:

- Analyze enterprise data using precise SQL filters
- Investigate security events with real-world logic
- Apply best practices in data-driven incident response
- Through these SQL queries, I demonstrated efficiency in filtering structured datasets to aid decision-making in security operations and infrastructure hardening.
  
---

## Let's Connect

I'm seeking entry-level roles in IT Security, Data Analysis, or SOC Operations where I can contribute with my SQL, investigative, and analytical skills.

- **Email:** jovaan.jwhitton@gmail.com
- **LinkedIn**: [linkedin.com/in/jovaan-whitton-profile](https://linkedin.com/in/jovaan-whitton-profile)
