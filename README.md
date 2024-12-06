# Project Overview

This project is a simple application for managing user logins, registrations, and laboratory test information. It uses JavaFX for the graphical user interface (GUI), MySQL for data storage, and Java for backend logic. The application allows users to log in, register, and interact with data related to laboratory tests.

## Technologies Used

### 1. **JavaFX for User Interface (UI) Development**
   - **JavaFX** is used to create the graphical user interface (GUI). It allows for the development of interactive, desktop applications.
   - **GridPane Layout**: A flexible layout manager to arrange the components (buttons, labels, text fields) in rows and columns.
   - **Event Handling**: JavaFX event handling for button clicks and user interactions.
   - **Scene and Stage**: The `Scene` represents the content of the window, and the `Stage` is the window itself.

### 2. **SQL for Database Management**
   - **MySQL** is used to store user data and laboratory test information.
   - **Tables**:
     - **`patient`**: Stores user data (e.g., ID, name, email, password).
     - **`labotest`**: Stores laboratory test details (e.g., test ID, type, price, options).
   - **SQL Operations**: 
     - **INSERT**: Adds new laboratory test records.
     - **SELECT**: Retrieves all records from the `labotest` table.
     - **UPDATE**: Modifies existing test records.
     - **DELETE**: Deletes test records based on test ID.
   - **Prepared Statements**: Used to safely execute SQL queries, preventing SQL injection attacks.
   - **Connection Handling**: Uses `JDBC` to manage database connections and execute queries.

### 3. **Password Hashing with MD5**
   - **MD5** hashing is used to secure user passwords by converting them into a fixed-length hash value before storing them in the database.
   - The `MD5.getMd5()` method hashes the password and returns a hashed string for secure storage.

### 4. **Java Classes and Object-Oriented Design**
   - The project follows an object-oriented design with several classes:
     - **LoginFrm**: Handles the user login form.
     - **PatientRegisterFrm**: Handles user registration.
     - **Labotest**: Represents laboratory tests, with properties like ID, type, price, and options.
     - **dbAdmin**: Handles database operations (inserting, selecting, updating, and deleting laboratory test records).
     - **MD5**: Contains the password hashing method.
   - **Data Validation**: Ensures that login and registration fields are not empty before proceeding with actions.

### 5. **Error Handling and Debugging**
   - **Try-Catch Blocks**: Error handling is implemented to catch exceptions during database operations or other program logic, preventing crashes and providing debug messages.

### 6. **Security Features**
   - **Password Hashing**: Uses MD5 hashing to securely store passwords in the database, ensuring they are not stored in plaintext.
   - **SQL Injection Prevention**: Prepared statements are used to prevent SQL injection attacks when interacting with the database.

### 7. **Database Design**
   - **Database**: MySQL database named `clinic`.
   - **Tables**:
     - `patient`: Stores user data (ID, name, password, email, etc.).
     - `labotest`: Stores laboratory test information (ID, type, price, options).
     - The connection to the database is managed by `dbConnection` class using JDBC.

---

## Getting Started

### Prerequisites
1. **Java Development Kit (JDK)**: Install JDK 8 or later.
2. **MySQL Database**: Set up a MySQL database server and create the `clinic` database.
3. **IDE**: Use any Java IDE (e.g., IntelliJ IDEA, Eclipse) to run the project.

### Database Setup

1. Create a MySQL database named `clinic`:
   ```sql
   CREATE DATABASE clinic;
