#  Employee Management System (Java Swing + MySQL)

A desktop-based **Employee Management System** built using **Java Swing** for the user interface and **MySQL** as the backend database.  
This application provides a complete GUI for managing employees, holidays, meetings, and overtime requests.

It features two user roles:
-  **Standard Employee (Non-HR)**
-  **Administrator (HR)**

Each role has its own interface and permissions.

---

##  Key Features

###  Standard Employee (Non-HR)
- **Secure Login:** Authenticate using an Employee ID and password.
- **Profile Management:** View and update personal info (First Name, Last Name, Address, Gender, Password).
- **Holiday Requests:**
  - Submit new holiday requests with start and end dates.
  - View request status (**Pending**, **Accepted**, or **Declined**).
- **Meeting Requests:**
  - Request meetings by date, start time, and end time.
  - View approval status.
- **Overtime Requests:**
  - Submit overtime (morning and evening hours) for a given date.
  - Track approval status.

---

###  HR Administrator
Includes **all features of Standard Employees**, plus:
- **Employee Administration:**
  -  Add new employees with full details, salary, and account type (HR / Non-HR).
  -  Remove employees by ID.
  -  Search and edit employee details (including password & salary).
- **Approval Portal:**
  - Review and approve or decline **Holiday**, **Meeting**, and **Overtime** requests from all employees.
- **System-wide View:**
  - View all holidays, meetings, or overtime records.
  - Filter records by Employee ID.

---

##  Technologies Used

| Category | Technology |
|-----------|-------------|
| **Frontend (GUI)** | Java Swing |
| **Backend** | Java (JDK 13) |
| **Database** | MySQL |
| **Build Tool** | Apache Maven |
| **Connector** | `mysql-connector-java` |

---

##  Prerequisites

Ensure you have the following installed:

- **Java Development Kit (JDK)** 13 or newer  
- **Apache Maven** (for build & dependencies)  
- **MySQL Server** (running on default port `3306`)

---

##  Installation & Setup

###  Clone the Repository
```bash
# Replace with your repository URL
git clone https://github.com/Simoni03/Employee-Management-System-Java-SQL.git
cd Employee-Management-System-Java-SQL/EmployeeManagementSystemJava
```

### 2 Set Up the Database

1 Start MySQL Server
Ensure MySQL is running (via XAMPP, MySQL Workbench, or as a service).

2 Create Database & Tables
Run the SQL script provided in:

``` bash
SQL database files/CreateDatabase.sql
```

Example using MySQL CLI:
```bash
mysql -u root -p < "../SQL database files/CreateDatabase.sql"
```
3 Database Connection Credentials
The app connects using the following defaults:
Database: sql_employees
URL: jdbc:mysql://localhost:3306/sql_employees
Username: root
Password: "" (empty)

### 3️ Build the Project

Use Maven to compile the code and download dependencies:
```bash
mvn clean install
```

### Running the Application
Run via Maven (using the main class defined in nbactions.xml):
mvn exec:java -Dexec.mainClass="GUI.General.GUIRunner"

Once launched, you’ll see the Login Page.
