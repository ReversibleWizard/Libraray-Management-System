LIBRARY MANAGEMENT SYSTEM
# Library Management System
Developed using Python and MYSQL

This project is a **Library Management System** built with Python and MySQL. It enables library administrators to efficiently manage books and student registrations, handle book issuances and returns, and display book records through a terminal-based interface.

---

## Features

1. **Add Book**: Add a new book to the library database.
2. **Issue Book**: Issue books to students and track the issuance date.
3. **Submit Book**: Record the return of books and calculate any applicable late fees.
4. **Delete Book**: Remove a book entry from the database.
5. **Display Books**: View all books available in the library.
6. **Student Registration**: Register new students in the library system.
7. **Password Protected**: Access to the application is secured with a password.

---

## Prerequisites

- **Python 3.x**: Install Python from [python.org](https://www.python.org/).
- **MySQL Server**: Install MySQL from [mysql.com](https://www.mysql.com/).
- **Required Python Libraries**:
  - `mysql-connector`
  - `pandas`
  - `datetime`

Install the libraries using the following command:
```bash
pip install mysql-connector-python pandas
```

---

## Setup and Configuration

1. **Database Setup**:
   - Create a database named `mydb_library` in MySQL.
   - Define the following stored procedures in your MySQL database:
     - `proc_bookresigtration`
     - `proc_bookissue`
     - `proc_bookreturn`
     - `proc_bookdelete`
     - `proc_studentregistration`

2. **Modify Database Connection**:
   Update the `create_server_connection` function in the script to include your MySQL credentials:
   ```python
   connection = create_server_connection("localhost", "root", "your_password", "mydb_library")
   ```

3. **Run the Script**:
   Execute the script using:
   ```bash
   python library_manager.py
   ```

4. **Password**:
   The default password to access the system is `XYZ@SCHOOL`.

---

## Usage Instructions

1. Run the script and enter the password to access the system.
2. Choose an option from the menu to perform the desired task:
   - Add a book by providing the book name, code, total copies, and subject.
   - Issue a book by entering the student's registration number, book code, and issuance date.
   - Return a book by providing the registration number, book code, and return date.
   - Delete a book by entering its code (only if it is not issued).
   - Display all books in the library.
   - Register a new student by entering their name and registration number.
3. The application will return to the main menu after each task.

---

## Code Structure

- `create_server_connection`: Establishes a connection to the MySQL database.
- `addbook`: Adds a new book to the library using the `proc_bookresigtration` stored procedure.
- `issueb`: Issues a book to a student using the `proc_bookissue` stored procedure.
- `submitb`: Records a book return using the `proc_bookreturn` stored procedure.
- `dbook`: Deletes a book using the `proc_bookdelete` stored procedure.
- `dispbook`: Displays all books in the library.
- `studentreg`: Registers a new student using the `proc_studentregistration` stored procedure.
- `pswd`: Handles password authentication.
- `main`: Displays the menu and manages user navigation.

---

## Known Issues and Future Improvements

1. **Stored Procedure Validation**:
   Ensure all stored procedures are implemented correctly in the database.
2. **Error Handling**:
   Improve error messages for better debugging.
3. **Password Security**:
   Replace the plaintext password with a hashed password for enhanced security.
4. **Resource Management**:
   Ensure the database connection is properly closed after each operation.
5. **GUI Interface**:
   Develop a graphical user interface for better user experience.

---

## License
This project is open-source and available for educational purposes. Feel free to use and modify it as needed.

---

## Author
**Sayak**
- B.Tech in Computer Science and Communication Engineering, KIIT University.


