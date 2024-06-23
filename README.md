# Attendance-System
An Automated Attendance Management System is designed to streamline and simplify the  process of recording, tracking, and managing attendance in educational institutions. This  system replaces traditional methods such as manual roll calls or paper registers, thereby  reducing errors, saving time, and providing more accurate data. 
Roles and Functionality:
First the user has to select from the two given roles that lead to further pages and operations to be performed
Admin Role:
o	Admin Login Page: Upon selecting the Admin role, the user is directed to the Admin login page.
o	Admin Dashboard: After successful login, the Admin dashboard is displayed.
o	User Management:
	Add Users: Admin can add new users to the application, including faculty members.
	Remove Users: Admin can also remove existing users from the application.
Faculty Role:
o	Faculty Login Page: Upon selecting the Faculty role, the user is directed to the Faculty login page.
o	Faculty Home Page: After successful login, the Faculty home page is displayed.
o	Attendance Page: From the home page, faculty members can navigate to the attendance page where the attendance marking process begins.
	Department Selection: Faculty members first select the relevant department.
	Course and Section Selection: Following the department selection, they choose the specific course and section.
	Mark Attendance: Faculty members can then mark the attendance for the selected course and section.
	Download Attendance Sheet: After marking the attendance, the attendance sheet can be downloaded for record-keeping and further processing.
Project Synchronization with topics
Refactoring Techniques Applied (attendance-page):
1.	JavaScript Modularization: Kept JavaScript functions concise and focused on specific tasks (selectDepartment, selectCourse, markAttendance, downloadAttendance).
2.	HTML Structure: Maintained a clear structure in HTML with distinct sections (departments, courses, attendanceTables) for better readability and manageability.
3.	Dynamic Element Creation: Utilized DOM manipulation to dynamically create table rows and manage visibility (display: none/block) based on user actions, enhancing user experience.
4.	Event Handling: Employed inline event listeners (onclick) for simplicity and clarity in function invocation.
5.	File Download Functionality: Implemented a robust file download mechanism using Blob objects and Object URLs, ensuring efficient handling of CSV data for attendance records.
Explanation of Concurrency Management Techniques (login-page):
1.	Asynchronous Function with async/await: Used async function for asynchronous handling. await is used to wait for the asynchronous fakeLogin function to complete before proceeding with further actions.
2.	Error Handling with try/catch: Implemented error handling to catch and manage any errors that might occur during the asynchronous operation (e.g., network issues, server errors).
3.	Promise-based Asynchronous Operation: Simulated a network request or database query using a Promise. This could represent a real async operation where data is fetched from a server.
4.	Role-based Redirect: After successful login, redirects are based on the role (admin or faculty) returned from the asynchronous operation.
5.	Simulated Delay: Included a setTimeout function inside fakeLogin to simulate network latency or server response delay. This is common in real-world applications to handle the asynchronous nature of network requests.
Exception handling (admin-page)
Password Length Validation:
•	Before adding a new user, the handleAddUserClick function now includes a loop to prompt the admin for a password and validate its length. It ensures that the password is at least 6 characters long.
•	If the entered password doesn't meet the length requirement, an alert is shown, and the admin is prompted again until a valid password is entered or the operation is canceled.
User Cancelation Handling:
•	If the admin cancels the password input prompt (by clicking Cancel or closing the prompt dialog), the function exits without adding a new user.
Maintained Functionality:
•	The functionality to add users, render the user table, delete users, and display the password (for demo purposes) remains unchanged.
•	The refactoring focuses on enhancing the user experience by enforcing a minimum password length requirement and handling user cancelation gracefully.
Access Key Validation:
•	When the handleAddUserClick function is triggered by clicking the "Add New User" button, it first prompts the user to enter an access key.
•	If the access key entered does not match '0000', an alert is shown indicating that the operation has been canceled.
SOLID Principles (Home-page):
1.	Single Responsibility Principle (SRP):
o	Each HTML element and CSS rule is responsible for a specific aspect of presentation or functionality. For instance, <header> manages the page header, while <main> contains the main content.
2.	Open/Closed Principle (OCP):
o	The design allows for extension without modification. You can add more  sections or pages (<section>, <footer>) without altering existing HTML or CSS significantly.


