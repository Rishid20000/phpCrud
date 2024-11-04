RNotes - Notes Taking Made Easy
RNotes is a simple CRUD (Create, Read, Update, Delete) application for managing notes. It allows users to add, edit, delete, and view notes using a user-friendly interface powered by PHP and MySQL.

Project Overview
This project demonstrates the basics of a PHP and MySQL-based CRUD application, incorporating data display using DataTables for easy sorting and searching. Users can manage notes, which include a title and a description, and perform operations such as adding new notes, updating existing ones, and deleting unwanted notes.

Features
Add Notes: Users can add a new note with a title and description.
Edit Notes: Users can edit the title and description of an existing note.
Delete Notes: Users can delete any note.
DataTables Integration: All notes are displayed in a DataTable, making it easy to search and sort through them.
Prerequisites
XAMPP (or another server stack with PHP and MySQL):
Download XAMPP from Apache Friends and install it.
Basic HTML, PHP, and MySQL Knowledge:
Familiarity with PHP and MySQL will help you understand and modify this project as needed.
Installation and Setup
Clone the Repository:

Download the code and place it in the htdocs folder of your XAMPP installation directory.
Database Setup:

Start the Apache and MySQL modules from the XAMPP Control Panel.
Go to http://localhost/phpmyadmin and create a new database called notes.
Import the following SQL script to create the notes table:
sql
Copy code
CREATE TABLE `notes` (
  `sno` int(11) NOT NULL AUTO_INCREMENT,
  `title` varchar(255) NOT NULL,
  `description` text NOT NULL,
  `tstamp` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  PRIMARY KEY (`sno`)
);
Configuration:

Ensure your database connection details are correctly set in the PHP file:
php
Copy code
$servername = "localhost";
$username = "root";
$password = "";
$database = "notes";
Run the Application:

Open your web browser and go to http://localhost/crud/index.php to view and interact with the application.
How It Works
Add a Note: Use the form at the top to enter a title and description, then click "Add Note."
Edit a Note: Click the "Edit" button next to any note, make changes in the pop-up form, and save.
Delete a Note: Click the "Delete" button next to any note to remove it. You will need to confirm the deletion.
Dependencies
Bootstrap 4: For styling and responsiveness.
DataTables: For enhanced table functionality (sorting and searching).
jQuery: Required for DataTables and modal functionality.
Notes
To edit or delete notes, ensure JavaScript is enabled in your browser for smooth modal interactions.
Data persistence is handled by a MySQL database, so ensure your server is running.
