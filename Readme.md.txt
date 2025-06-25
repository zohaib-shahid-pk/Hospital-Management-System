1 Hospital Management System (SQLite Project)

This project is a simple Hospital Management System using SQLite. It includes three main tables to manage hospital data:

- Patients
- Doctors
- Appointments

The goal is to store, manage, and retrieve information about patients, doctors, and their appointment schedules using SQL queries.

---

2  Project Files

- `hospital.db` – SQLite database file
- `schema.sql` – Contains the CREATE TABLE scripts
- `sample_queries.sql` – Sample queries to fetch data from the database

---

3  Technologies Used

- SQLite (Local database engine)
- SQLite Command-Line Tool

---

4  Table Structure

### 1. Patients
| Column       | Type     |
|--------------|----------|
| patients_id  | INTEGER (Primary Key) |
| name         | TEXT     |
| age          | INTEGER  |
| gender       | TEXT     |
| phone        | TEXT     |

### 2. Doctors
| Column       | Type     |
|--------------|----------|
| doctor_id    | INTEGER (Primary Key) |
| name         | TEXT     |
| specialization | TEXT   |

### 3. Appointments
| Column         | Type     |
|----------------|----------|
| appointment_id | INTEGER (Primary Key) |
| patients_id    | INTEGER (Foreign Key) |
| doctors_id     | INTEGER (Foreign Key) |
| appointment_date | TEXT  |

---

5  Sample Query

	sql
SELECT p.name, p.age, p.gender, d.name, d.specialization
FROM patients p
JOIN appointment a ON p.patients_id = a.patients_id
JOIN doctors d ON a.doctors_id = d.doctor_id;
