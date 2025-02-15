# Library Management System

## Overview
This project sets up a relational database called `Library` to manage library operations, including branches, employees, customers, books, and issue/return statuses. It includes SQL scripts for database creation, table definitions, data insertion, and key queries to retrieve useful information.

## Database Schema
### Tables
1. **Branch**
   - Stores information about different library branches.
   - Attributes: `Branch_no`, `Manager_id`, `Branch_address`, `Contact_no`.

2. **Employee**
   - Stores details about library employees.
   - Attributes: `Emp_id`, `Emp_name`, `Position`, `Salary`, `Branch_no` (linked to Branch table).

3. **Customer**
   - Stores customer details.
   - Attributes: `Customer_Id`, `Customer_name`, `Customer_address`, `Reg_date`.

4. **Books**
   - Stores details of books available in the library.
   - Attributes: `ISBN`, `Book_title`, `Category`, `Rental_Price`, `Status`, `Author`, `Publisher`.

5. **IssueStatus**
   - Tracks book issuance records.
   - Attributes: `Issue_Id`, `Issued_cust` (FK to Customer), `Issued_book_name`, `Issue_date`, `Isbn_book` (FK to Books).

6. **ReturnStatus**
   - Tracks book return records.
   - Attributes: `Return_id`, `Return_cust`, `Return_book_name`, `Return_date`, `isbn_book2` (FK to Books).

## Data Insertion
Predefined sample records are inserted into the `Branch`, `Employee`, `Customer`, `Books`, `IssueStatus`, and `ReturnStatus` tables.

## Queries
1. Retrieve available books with title, category, and rental price.
2. List employees and salaries in descending order.
3. Retrieve book titles and corresponding customers who issued them.
4. Count of books per category.
5. Retrieve employees with salaries above Rs. 50,000.
6. List customers registered before 2022-01-01 who haven't issued books.
7. Display branch numbers and employee counts per branch.
8. List customers who issued books in June 2023.
9. Retrieve book titles categorized under 'History'.
10. Display branches with more than five employees.

## Additional Features
- Foreign key constraints ensure referential integrity.
- Status tracking for book availability.
- Automatic updates when issuing or returning books.

## Setup Instructions
1. Run the SQL script in a MySQL environment.
2. Verify tables using `SHOW TABLES;`.
3. Perform queries for library management insights.

## Conclusion
This project effectively organizes a library system, enabling efficient book issuance, return tracking, and employee management through structured SQL queries.


