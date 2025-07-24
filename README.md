# 💃 Dance Workshop Management System

A full-stack Dance Workshop Management System developed using **HTML, CSS, PHP, and MySQL**. This platform allows dance academies to efficiently manage dance styles, batches, student registrations, and workshop schedules.

---

## 📸 Screenshots

### 🖥️ Home Page
![Home Page](screenshots/homepage.png)

### 🔐 Admin Login
![Admin Login](screenshots/admin-login.png)

### 📊 Admin Dashboard
![Dashboard](screenshots/dashboard.png)

### 📝 Manage Dance Styles
![Manage Styles](screenshots/manage-styles.png)

---

## 🛠️ Tech Stack

- **Frontend**: HTML5, CSS3, Bootstrap  
- **Backend**: PHP  
- **Database**: MySQL  
- **Web Server**: Apache (XAMPP/WAMP)

---

## ✨ Features

- 🔐 Secure admin login system
- 🕺 Add/edit/delete dance styles and categories
- 👨‍🎓 Manage student registrations and batches
- 🗓️ Schedule dance workshops
- 📋 Fully functional CRUD system
- 📊 Dashboard to view analytics and manage entities

---

## 📁 Project Structure

danceworkshop/
├── admin/ # Admin dashboard and modules
├── css/ # Stylesheets
├── images/ # UI assets
├── includes/ # DB connection, session handling
├── index.php # Homepage
├── login.php # Admin login
├── register.php # Registration form
└── ...

---

## 🚀 How to Run Locally

### 🔧 1. Clone the Repository

git clone https://github.com/gawalishankar/Dance-Workshop-Project.git
cd Dance-Workshop-Project/danceworkshop-master/danceworkshop
🖥️ 2. Set Up Local Server
Install XAMPP or WAMP

Move the danceworkshop folder into htdocs (XAMPP) or www (WAMP)

🗃️ 3. Import Database
Open http://localhost/phpmyadmin

Create a new database named danceworkshop

Import the SQL file: danceworkshop.sql (if included)

⚙️ 4. Configure Database Connection
Open includes/dbconnection.php and set:

$host = "localhost";
$db_user = "root";
$db_pass = "";
$db_name = "danceworkshop";
🙋 Author
Name: Shivshankar Gawali

GitHub: @gawalishankar

LinkedIn: linkedin.com/in/your-profile

📄 License
Licensed under the MIT License.

