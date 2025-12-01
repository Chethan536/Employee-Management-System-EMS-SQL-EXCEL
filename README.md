# Employee Management System (EMS)

### **End-to-End SQL + Excel Data Analysis Project**

---

## 📌 **Project Overview**

This project demonstrates a complete **Employee Management System (EMS)** built using:

* **SQL** (MySQL Workbench)
* **Excel** (Data cleaning, transformation, reporting)
* **Pivot Tables & Lookups**

It covers the full workflow from **database design → data extraction → transformation → reporting & insights**.

The EMS manages:

* Employee information
* Job roles & departments
* Salary, bonus & payroll
* Qualifications
* Leave management

This repository showcases both **technical depth** (SQL engineering) and **analytical capability** (Excel dashboards).

---

## 🗂️ **Project Structure**

```
EMS_Project/
│
├── SQL_Schema/               → Database schema & DDL scripts
├── SQL_Analysis/             → Analytical SQL queries & insights
├── Excel_Files/              → Exported tables, Master_Data, Pivot Reports
├── Report/                   → Final EMS Report (PDF)
└── README.md                 → Project documentation
```

---

## 🏗️ **1. SQL Phase — Database Design**

The EMS database contains **6 relational tables**:

1. **JobDepartment** – Department, job roles & salary ranges
2. **SalaryBonus** – Salary, annual pay, bonuses per job
3. **Employee** – Employee personal & job details
4. **Qualification** – Employee skills & qualifications
5. **Leaves** – Leave records & reasons
6. **Payroll** – Final payroll computation

### 🔗 **ER Diagram (Conceptual)**

```
JobDepartment ← SalaryBonus
        ↑            ↑
        |            |
     Employee ← Qualification
        ↓
      Leaves
        ↓
      Payroll
```

### 🛡️ Key Features

* Foreign key constraints with **CASCADE** rules
* Email uniqueness constraint
* Automatic payroll linkage through Job_ID & Salary_ID
* Clean normalization (1NF–3NF)

---

## 📊 **2. SQL Insights Generated**

Using advanced SQL joins, aggregations, and filtering, the following insights were derived:

### 👥 Employee Insights

* Total employees: **60**
* Top departments by size: **Finance**, **IT**
* Highest paid employees list
* Average age, salary & distribution

### 💼 Department & Job Role Insights

* Department with most job roles: **Finance**
* Highest salary roles: **Department Directors & Senior Leads**

### 📘 Qualification Insights

* Each employee has at least one qualification
* Required skills per job role

### 📝 Leave Insights

* Total company-wide leaves: **60**
* Average leave per employee: **1 day**

### 💰 Payroll Insights

* Monthly net payroll: **$2.77M**
* Highest bonus allocation: **Legal & Finance**

---

## 📥 **3. Excel Phase — Data Transformation**

After exporting SQL tables to Excel:

* Cleaned and standardized all datasets
* Removed formatting issues & table artifacts
* Created a unified **Master_Data** file

### 🔍 **Lookup Columns Added**

Using VLOOKUP formulas:

#### Department Lookup

```
=VLOOKUP(Job_ID, jobdepartment!A:B, 2, FALSE)
```

#### Salary Lookup

```
=VLOOKUP(Job_ID, salarybonus!B:C, 2, FALSE)
```

#### Bonus Lookup

```
=VLOOKUP(Job_ID, salarybonus!B:E, 4, FALSE)
```

#### Payroll Lookup

```
=VLOOKUP(Emp_ID, payroll!B:H, 7, FALSE)
```

---

## 📈 **4. Excel Reporting — Pivot Tables & Dashboards**

Three interactive dashboards were created:

### **4.1 Department Headcount**

* Shows number of employees per department

### **4.2 Department Salary Cost Summary**

* Total salary spend per department
* Salary distribution comparison

### **4.3 Employee Payroll Summary**

* Salary, bonus, and total payout per employee
* Department-wise aggregation

---

## 🎯 **5. Final Business Insights**

* Highest salary cost departments → **Finance, IT**
* Highest bonuses → **Legal department**
* Payroll totals align with SQL outputs (**full system consistency achieved**)
* HR managers can easily track workforce distribution & compensation structure

---

## 🚀 **6. Skills Demonstrated**

### **SQL Skills**

* Data modeling
* DDL & DML scripting
* Normalization & relationships
* JOINS, aggregate queries, subqueries
* Constraint management

### **Excel Skills**

* Data cleaning & transformation
* VLOOKUP / XLOOKUP mappings
* Pivot tables
* HR analytics dashboards

### **Analytical Skills**

* Data validation & integration
* Payroll and compensation analysis
* Department-level workforce insights

---

## 📄 **7. How to Use This Repository**

1. Import SQL schema into MySQL Workbench
2. Run all INSERT scripts
3. Export tables using CSV
4. Open the Excel folder → `Master_Data.xlsx`
5. Explore Pivot tables for insights

---

## 📘 **8. Future Enhancements**

* Power BI dashboard version
* Integration with Python (Pandas + SQLAlchemy)
* Automated payroll calculation using stored procedures
* Flask/Django mini-application

---

## 👤 **Author**

**Chethan Vakiti**
Data Analyst | SQL | Python | Excel | Power BI

