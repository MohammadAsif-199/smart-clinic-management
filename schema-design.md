# Smart Clinic – Database Schema Design

This file defines the **MySQL database schema** for the Smart Clinic application.  
The schema covers `Doctor`, `Patient`, `Admin`, `Appointment`, and `Prescription` tables.

---

## Doctor Table
```sql
CREATE TABLE Doctor (
    doctor_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    specialization VARCHAR(100) NOT NULL,
    email VARCHAR(100) UNIQUE NOT NULL,
    phone VARCHAR(15),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

