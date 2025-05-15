# Student Filter Application using PostgreSQL and Appsmith

This project demonstrates how to create a dynamic student filtering web application using a PostgreSQL database hosted on **Render** and a frontend interface built with **Appsmith**.

---

## 📌 Overview

The application allows users to:

- View a list of students from a PostgreSQL database.
- Filter students based on:
  - **School Name**
  - **Class**
  - **Section**

It uses dropdown menus for filtering and displays the results in a table dynamically.

---

## 🧰 Technologies Used

- **Render** – Cloud PostgreSQL hosting
- **pgAdmin 4** – GUI for managing PostgreSQL
- **PostgreSQL** – Relational database
- **Appsmith** – Low-code tool to create internal applications

---

## 🔧 Setup Instructions

### 1. PostgreSQL Setup on Render

- Sign up at [Render.com](https://render.com).
- Create a **PostgreSQL** database:
  - **Name**: `student_database`
  - **Database**: `students`
  - **User**: `admin`
  - **Version**: Latest (e.g., 15)
- Save the **External Database URL** for later use.

### 2. Connect Render DB to pgAdmin

- Install **pgAdmin 4** from [pgadmin.org](https://www.pgadmin.org/download/).
- Register a new server in pgAdmin:
  - Use the database URL parts for host, username, and password.
- Create a table named `student_data` with the following schema:

```sql
CREATE TABLE student_data (
  id INTEGER PRIMARY KEY,
  school_name VARCHAR(100),
  class VARCHAR(10),
  section VARCHAR(5),
  student_name VARCHAR(100),
  roll_number INTEGER
);
