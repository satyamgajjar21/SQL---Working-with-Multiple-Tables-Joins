# 📚 SQL Essentials: Working with Multiple Tables & Joins

Welcome to this hands-on lab on **Working with Multiple Tables** in SQL! This repository contains a step-by-step guide on how to write SQL queries that access multiple tables, compose queries using sub-queries and implicit joins, and much more. Whether you are a beginner or looking to deepen your SQL skills, this guide is perfect for you!

---

## 🛠️ What You’ll Learn
After completing this lab, you'll be able to:
- Write SQL queries that access multiple tables
- Compose queries using nested statements in the `WHERE` clause
- Build queries with multiple tables in the `FROM` clause
- Write **Implicit Join** queries with join criteria specified in the `WHERE` clause
- Use **table aliases** to qualify column names

---

## 🗂️ Software & Database Used
- **Software**: MySQL (Relational Database Management System)
- **Lab Platform**: IBM Skills Network Labs (Cloud IDE)
- **Database**: Sample HR Database

---

## 🏗️ Step-by-Step Instructions

### 1. **Create the Database**
Follow the steps below to set up your environment in **phpMyAdmin**:

1. Open phpMyAdmin from the Skills Network Toolbox in the Cloud IDE.
2. Create a blank database named **HR**.
3. Use the script provided to create the required tables for this lab. 
    - **[Script_Create_Tables.sql](#)**

### 2. **Load Data into Tables**
Download and upload the following files for the respective tables:
- **Departments.csv**
- **Jobs.csv**
- **JobsHistory.csv**
- **Locations.csv**
- **Employees.csv**

### 3. **Accessing Multiple Tables with Sub-Queries**
Here are some queries that will help you access data from multiple tables using sub-queries.

#### Example 1: Retrieve Employees with Specific Jobs
```sql
SELECT * 
FROM EMPLOYEES
WHERE JOB_ID IN (SELECT JOB_IDENT FROM JOBS);
