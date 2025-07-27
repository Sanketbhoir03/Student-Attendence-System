Student Attendance Management System
This project is a web-based Student Attendance Management System designed to streamline the process of tracking student attendance for educational institutions. It provides interfaces for administrators, teachers, and students to manage and view attendance records efficiently.

Features
Admin Module:

Manage students (add, edit, delete student records).

Manage teachers (add, edit, delete teacher accounts).

Manage courses/subjects.

View attendance reports.

Teacher Module:

Mark attendance for students in their assigned subjects.

View their assigned students.

View attendance records.

Manage their password.

Student Module:

View their attendance records.

Manage their password.

User Authentication: Secure login for different user roles (admin, teacher, student).

Database Integration: Stores and retrieves data from a MySQL database.

Technologies Used
Backend: PHP

Frontend: HTML, CSS, JavaScript

Database: MySQL (or compatible SQL database)

JavaScript Libraries/Frameworks (Potential): GSAP (based on adminPage.js) for animations.

Project Structure
The project is organized into the following main directories:

admin/: Contains PHP files for the administrator's interface (e.g., admin.php, course.php, student.php, teacher.php, subjects.php, year.php).

include/: Contains common PHP files like database connection (dbcon.php), header (header.php, studentHeader.php, teacherHeader.php), session management (session.php), and logout (logout.php).

js/: Contains JavaScript files for front-end interactivity (e.g., adminPage.js, loginPage.js).

student/: Contains PHP files for the student's interface (e.g., home.php, managePassword.php, record.php, report.php).

teacher/: Contains PHP files for the teacher's interface (e.g., attendance.php, home.php, record.php, report.php, students.php).

student_attendance_management.sql: The SQL dump file for setting up the database.

index.php: The main entry point of the application, likely handling the login.

Setup Instructions
To set up and run this project on your local machine, follow these steps:

Prerequisites
Web Server: Apache or Nginx (with PHP support)

PHP: Version 7.x or higher recommended.

Database Server: MySQL or MariaDB.

Composer (Optional but Recommended): For PHP dependency management, if any are used.

Installation Steps
Clone or Download the Project:
Download or clone the project files to your web server's document root (e.g., htdocs for Apache, www for Nginx).

# If using Git
git clone <repository_url> student-attendance-management

Database Setup:

Create a new MySQL database (e.g., student_attendance_db).

Import the student_attendance_management.sql file into your newly created database. You can do this using phpMyAdmin or the MySQL command line:

mysql -u your_username -p student_attendance_db < student_attendance_management.sql

(Replace your_username and student_attendance_db with your actual credentials and database name.)

Configure Database Connection:

Navigate to the include/ directory.

Open dbcon.php and update the database connection details (database name, username, password, host) to match your setup.

<?php
// Example dbcon.php content (adjust as per actual file)
$servername = "localhost"; // Your database host
$username = "root";        // Your database username
$password = "";            // Your database password
$dbname = "student_attendance_db"; // Your database name

// Create connection
$conn = new mysqli($servername, $username, $password, $dbname);

// Check connection
if ($conn->connect_error) {
    die("Connection failed: " . $conn->connect_error);
}
?>

Access the Application:
Open your web browser and navigate to the project's URL. If you placed it in your web server's root, it might be:

http://localhost/student-attendance-management/

You should see the login page.

Usage
Login: Use the provided login page to access different modules. Default credentials might be available in the student_attendance_management.sql file or need to be created manually in the database.

Admin: Manage all aspects of the system, including user accounts, courses, and overall reports.

Teacher: Mark attendance for their classes and view student records.

Student: View their personal attendance history.

Contributing
(Optional section - if you plan to allow contributions)
Contributions are welcome! If you'd like to contribute to this project, please follow these steps:

Fork the repository.

Create a new branch (git checkout -b feature/your-feature-name).

Make your changes.

Commit your changes (git commit -m 'Add new feature').

Push to the branch (git push origin feature/your-feature-name).

Create a Pull Request.
