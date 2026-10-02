# 🏫 SOS – School of Skills Management Portal

A web-based **Institution Management System** built using **Python and Streamlit** for managing students, courses, employees, enrollment, attendance, fees, and institutional reports.

The application provides a centralized dashboard with an interactive interface for managing academic and administrative activities.

---

## 🚀 Features

### 📊 Dashboard

* View total students
* View total employees
* View total courses
* View total enrollments
* Monitor student attendance
* Monitor employee attendance
* Course-wise enrollment visualization
* Recent activity tracking
* Quick navigation actions

### 🏛️ Institution Management

* Institution information
* Location and establishment details
* Contact information
* Department listing
* Institution overview

### 🎓 Student Management

* Register new students
* View all students
* Search students by ID or name
* View student profiles
* Assign students to courses
* Track admission dates
* Monitor student status

### 📚 Course Management

* Add new courses
* View available courses
* Search courses by ID or name
* Track course capacity
* Monitor enrolled students
* Display available seats
* Assign faculty to courses

### 👨‍🏫 Employee Management

* Add employees
* View employee records
* Search employees
* Manage departments
* Manage designations
* Track specialization
* Track employment type
* Assign courses to faculty

### 📝 Enrollment Management

* Enroll students into courses
* Drop students from courses
* Track enrollment records
* Monitor course capacity

The underlying OOP model keeps student and course enrollment synchronized through the `AcademicServices` layer.

### 📅 Attendance Management

* Student attendance
* Employee attendance
* Mark Present / Absent / Leave
* View attendance history
* Edit attendance records
* Generate attendance summaries
* Calculate attendance percentages

### 💰 Fee Management

* View fee records
* Record student payments
* Track total fees
* Track paid amounts
* Automatically calculate pending fees
* Display payment status:

  * Paid
  * Partially Paid
  * Pending

The fee system uses the paid amount as the source of truth and derives the pending amount from total fee minus paid fee.

### 📈 Reports & Analytics

The portal provides reports for:

* Student Report
* Employee Report
* Course Report
* Student Attendance Report
* Employee Attendance Report
* Enrollment Report
* Fee Report

### ⚙️ Administration

* System settings
* Data management
* Institution branding
* Reset/demo data management

---

## 🛠️ Technologies Used

* **Python**
* **Streamlit**
* **Pandas**
* **Object-Oriented Programming (OOP)**
* **Regular Expressions**
* **Python Dataclasses**
* **Session State Management**
* **Data Visualization**

---

## 📂 Project Structure

```text
SOS-School-of-Skills/
│
├── app.py
├── institution.py
├── README.md
└── requirements.txt
```

### `app.py`

Main Streamlit application containing the user interface, navigation, dashboard, student management, course management, employee management, attendance, fees, reports, and administration modules.

### `institution.py`

Contains the backend/domain models and OOP structure for:

* Institution
* Course
* Student
* Employee
* Faculty
* Academic Services

It also includes validation, enrollment handling, fee management, demo data, and self-tests.

---

## 🧠 Object-Oriented Design

The project uses OOP concepts to organize the institution's data and operations.

### Main Classes

```text
SOSInstitution
     │
     ├── Course
     │
     ├── Student
     │
     ├── Employee
     │      └── Faculty
     │
     └── AcademicServices
```

### Key OOP Concepts Used

* Classes and Objects
* Encapsulation
* Inheritance
* Properties
* Class Methods
* Static Methods
* Data Validation
* Service Layer Architecture

The `Student` model encapsulates fee information and provides validated payment handling through `record_payment()`.

---

## 🎨 User Interface

The application uses a **Red / Black / White** theme with:

* Responsive Streamlit layout
* Sidebar navigation
* Dashboard KPI cards
* Tables
* Forms
* Tabs
* Charts
* Status badges
* Search functionality

The application also uses a custom SOS logo and branded interface.

---

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/SOS-School-of-Skills.git
```

### 2. Navigate to the project

```bash
cd SOS-School-of-Skills
```

### 3. Create a virtual environment

```bash
python -m venv venv
```

### 4. Activate the virtual environment

**Windows:**

```bash
venv\Scripts\activate
```

**Linux / macOS:**

```bash
source venv/bin/activate
```

### 5. Install dependencies

```bash
pip install -r requirements.txt
```

### 6. Run the application

```bash
streamlit run app.py
```

The application will open in your browser.

---

## 📋 Requirements

Create a `requirements.txt` file containing:

```text
streamlit
pandas
```

If additional packages are added to the project later, update the requirements file accordingly.

---

## 🔄 Application Workflow

```text
                ┌─────────────────────┐
                │     SOS Portal      │
                └──────────┬──────────┘
                           │
              ┌────────────▼────────────┐
              │       Dashboard         │
              └────────────┬────────────┘
                           │
       ┌──────────┬────────┼────────┬──────────┐
       ▼          ▼        ▼        ▼          ▼
   Students    Courses  Employees Enrollment Attendance
       │          │        │        │          │
       └──────────┴────────┼────────┴──────────┘
                           ▼
                     Fee Management
                           │
                           ▼
                   Reports & Analytics
                           │
                           ▼
                     Administration
```

---

## 🔐 Data Handling

The current application uses **Streamlit session state** for storing and managing application data during a session.

Sample institution, course, student, employee, enrollment, attendance, and fee data are included for demonstration purposes.

> **Note:** This project is currently designed as a demonstration/academic management system and does not use a persistent production database.

---

## 🧪 Testing

`institution.py` includes built-in self-tests for:

* Fee calculation
* Payment validation
* Enrollment consistency
* Course dropping
* Student-course relationships

Run:

```bash
python institution.py
```

A successful test run prints:

```text
All institution.py self-tests passed — no errors.
```

---

## 🔮 Future Improvements

Possible future enhancements include:

* MySQL / PostgreSQL database integration
* User authentication and role-based access
* Admin and faculty login
* Persistent data storage
* Student login portal
* Online fee payment
* Email notifications
* PDF report generation
* Cloud deployment
* REST API integration
* Advanced analytics dashboard
* Database backup and recovery

---

## 👨‍💻 Author

**Ahmed Zayan**

B.Tech Computer Science Engineering
Currently pursuing Data Science training 

---

## 📄 License

This project is developed for **educational and academic purposes**.

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub.
