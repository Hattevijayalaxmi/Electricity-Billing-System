# Electricity Billing System – Core Java + MySQL (Desktop Based Application)

## 📌 Project Overview

The **Electricity Billing System** is a desktop-based application developed using **Core Java**, **Swing/AWT**, and **MySQL**.
It helps electricity departments manage customer details, generate bills, calculate electricity charges, and maintain payment records digitally.

---

# 🛠 Technologies Used

* Core Java
* Java Swing / AWT (GUI)
* MySQL Database
* JDBC Connectivity
* NetBeans / Eclipse / IntelliJ IDEA

---

# ✨ Main Features

## 👤 Customer Module

* Add New Customer
* Update Customer Details
* Delete Customer
* View Customer Information

## ⚡ Meter & Billing Module

* Enter Meter Reading
* Calculate Electricity Bill
* Generate Monthly Bill
* Print Bill Receipt

## 💳 Payment Module

* Bill Payment
* Payment History
* Due Amount Tracking

## 🔐 Admin Module

* Admin Login
* Manage Customers
* View Reports

---

# 🗂 Database Tables

## 1. Customer Table

```sql
create table customer(name varchar(20), meter_no varchar(20), address varchar(50), city varchar(30), state varchar(30), email varchar(40), phone varchar(20));

```

---

## 2. Meter Reading Table

```sql
create table meter_info(meter_no varchar(20), meter_location varchar(20), meter_type varchar(20), phase_code varchar(20), bill_type varchar(20), days varchar(20));

```

---

## 3. Bill Table

```sql
create table bill(meter_no varchar(20), month varchar(30), units varchar(20), totalbill varchar(20), status varchar(20));

```

---

# 🔌 JDBC Connection Code

```java
package electricity.billing.system;

import java.sql.*;

public class Conn {

    Connection c;
    Statement s;
    Conn() {
        try {
            c = DriverManager.getConnection("jdbc:mysql:///ebs", "root", "Shraddha@123");
            s = c.createStatement();
        } catch (Exception e) {
            e.printStackTrace();
        }
    }
}

```

---

# 🖥 Suggested GUI Screens

1. Login Page
2. Home Dashboard
3. Add Customer Form
4. Meter Reading Form
5. Generate Bill Page
6. Payment Page
7. View Bill History

---

# 📁 Recommended Project Structure

```text
ElectricityBillingSystem/
│
├── src/
│
├── BillDetails.java
├── CalculateBill.java
├── Conn.java
├── CustomerDetails.java
├── DepositeDetails.java
├── GenerateBill.java
├── Login.java
├── MeterInfo.java
├── NewCustomer.java
├── PayBill.java
├── Paytm.java
├── Project.java
├── Signup.java
├── Splash.java
├── UpdateInformation.java
└── ViewInformation.java
│
├── lib/
│   └── mysql-connector-java-8.0.28.jar
│
└── database/
    └── electricitybilling.sql
```

---

# 🎯 Advantages

* Reduces manual work
* Fast bill generation
* Secure customer data storage
* Easy payment tracking
* User-friendly desktop interface

---

# 📌 Resume Project Description

## Short Version

> Developed a desktop-based Electricity Billing System using Core Java, Swing, JDBC, and MySQL for customer management, bill generation, and payment tracking.

## Professional Version

> Designed and developed a desktop-based Electricity Billing System using Core Java, Java Swing, JDBC, and MySQL. Implemented modules for customer management, meter reading, bill calculation, payment tracking, and report generation with secure database connectivity.

---

# 💡 Extra Features You Can Add

* PDF Bill Generation
* Email Bill Notification
* Admin Dashboard Charts
* User Login Authentication
* Dark Mode UI
* Search & Filter Customers
 Connection Code
