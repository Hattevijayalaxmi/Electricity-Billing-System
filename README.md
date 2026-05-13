# Electricity Billing System – Core Java + MySQL (Desktop Based Application)

## 📌 Project Overview

The **Electricity Billing System** is a desktop-based application developed using **Core Java**, **Swing/AWT**, and **MySQL**.
It helps electricity departments manage customer details, generate bills, calculate electricity charges, and maintain payment records digitally.

---

# 🛠 Technologies Used

* Core Java
* Java Swing / AWT (GUI)
* MySQL Database / MySQL Workbeanch
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

## 1. Create Databases

```sql
create database ebs;

```

---

## 2. Use Databases

```sql
Use ebs;

```

---

## 3. Login Table

```sql
create table login(meter_no varchar(20), username varchar(30), name varchar(30), password varchar(20), user varchar(20)); 

```

---

## 4. Customer Table

```sql
create table customer(name varchar(20), meter_no varchar(20), address varchar(50), city varchar(30), state varchar(30), email varchar(40), phone varchar(20));

```

---

## 5. Meter Table

```sql
create table meter_info(meter_no varchar(20), meter_location varchar(20), meter_type varchar(20), phase_code varchar(20), bill_type varchar(20), days varchar(20));

```

---

## 6. Tax Table

```sql
create table tax(cost_per_unit varchar(20), meter_rent varchar(20), service_charge varchar(20), service_tax varchar(20), swacch_bharat_cess varchar(20), fixed_tax varchar(20));

```

---

## 7. Insert Tax

```sql
insert into tax values('9','47','22','57','6','18');

```

---

## 8. Bill Table

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

# 📁 Recommended Project Structure

```text
ElectricityBillingSystem/
│
├── src/
     └── BillDetails.java
     └── CalculateBill.java
     └── Conn.java
     └── CustomerDetails.java
     └── DepositeDetails.java
     └── GenerateBill.java
     └── Login.java
     └── MeterInfo.java
     └── NewCustomer.java
     └── PayBill.java
     └── Paytm.java
     └── Project.java
     └── Signup.java
     └── Splash.java
     └── UpdateInformation.java
     └── ViewInformation.java
│
├── lib/
│   └── mysql-connector-java-8.0.28.jar
|   └── rs2xml.jar
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

* Email Bill Notification
* Admin Dashboard Charts
* User Login Authentication
* Dark Mode UI
* Search & Filter Customers
 Connection Code
