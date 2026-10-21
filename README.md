# 🏥 PLP Clinic Monitoring System

A web-based application for managing and monitoring operations at the **Pamantasan ng Lungsod ng Pasig (PLP) Clinic**, including patient health records, daily transactions, item borrowing, and medicine inventory.

Developed as a school project by Group 5.

## 🎯 Purpose

* Replace paper-based clinic forms with a centralized digital system
* Track student and personnel visits, assessments, and medical history
* Monitor borrowed clinic items and medicine stock
* Give patients access to their own records through a user portal

## ✨ Features

**Authentication & Roles**
* Login system with three roles: **Admin**, **Staff**, and **User** (patient)
* Passwords hashed with PHP `password_hash()`

**Time In / Time Out**
* QR code scanning (via camera) to log clinic visits
* Reason-for-visit capture and daily transaction records

**Patient Records (Admin/Staff)**
* Student and personnel patient profiles
* Health Services Medical Form: emergency contact, family, surgical, smoking, alcohol, and drug history, and maternal history
* Patient assessment and visit records
* Printable/PDF record views (jsPDF)

**Borrowing**
* Borrow and return forms with photo capture
* Borrowing records and per-user borrowed items

**Inventory**
* Add, update, and delete clinic items and medicines
* Item summary charts

**Dashboard**
* Admin dashboard with patient and inventory charts (Chart.js)

**User Portal**
* Patients can view their medical history and borrowed items

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML, CSS, JavaScript |
| Backend | PHP (mysqli) |
| Database | MySQL |
| Libraries | SweetAlert2, Chart.js, jsPDF, Boxicons, Font Awesome |
| Server | Apache (XAMPP) |

## 📁 Project Structure

```
├── login.html / time_in.html    # Entry pages
├── forms-admin/                 # Admin/staff pages
├── forms-user/                  # Patient portal pages
├── popup-forms/                 # Assessment and medical record popups
├── php/                         # Auth, database connection, time in/out
├── php-admin/                   # Admin/staff API endpoints
├── php-user/                    # Patient portal endpoints
├── js/ js-admin/ js-user/       # Frontend scripts
├── css-user/ popup-styles/      # Stylesheets
├── db/clinic_system.sql         # Database schema
└── pictures/                    # Images and logos
```

## ⚙️ Setup

1. Install **XAMPP** (Apache + MySQL + PHP).
2. Clone this repo into your `htdocs` folder:
```
   git clone https://github.com/<your-username>/PLP-CLINIC-M-S.git
```
3. Start **Apache** and **MySQL** in XAMPP.
4. Create a database named `clinic_system` in phpMyAdmin and import `db/clinic_system.sql`.
5. Check the connection settings in `php/database.php` (host, user, password, database).
6. Create an `uploads/` folder in the project root (used for borrow/return photos).
7. Open `http://localhost/PLP-CLINIC-M-S/login.html`.

> The `.htaccess` file enables PHP inside `.html` files, so Apache must allow `.htaccess` overrides.

## 👥 Programmers: Group 5

* MIAH
* JAL
* KAIZEN
* CZYLA
* JEKKO

## 📬 Contact

For concerns about the system, please contact the PLP Clinic.
