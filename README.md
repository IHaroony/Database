# Library Management System

# Overview


This project implements a basic library management system using SQLite and Python. It manages data related to authors, books, borrowers, and book loans.

# Features
Database Schema: Includes tables for authors, books, borrowers, and loans.
Database Operations: Functions to add authors, books, borrowers, loan books, return books, and list records.
Database Schema
Tables
authors: Stores author details.
books: Stores book details, linked to authors.
borrowers: Stores borrower details.
loans: Records book loans, linked to books and borrowers.

# Setup
Create Database and Tables

Ensure you have library_schema.sql containing the table creation SQL script.
Run the script to create the database and tables using Python.

Dependencies

Python 3.x
sqlite3 (included with Python standard library)


# Functions
connect_db(): Connects to the SQLite database.
create_tables(): Creates tables if they don't exist.
add_author(name): Adds a new author.
add_book(title, author_id, publication_year, genre): Adds a new book.
add_borrower(name, email): Adds a new borrower.
loan_book(book_id, borrower_id, loan_date): Records a book loan.
return_book(loan_id, return_date): Updates a loan record with the return date.
list_books(): Lists all books with details.
list_borrowers(): Lists all borrowers.
list_loans(): Lists all loans with details.

# Example Usage
Create Tables

python
Copy code
create_tables()
Add Data

python
Copy code
add_author('J.K. Rowling')
add_book('Harry Potter and the Sorcerer\'s Stone', 1, 1997, 'Fantasy')
add_borrower('John Doe', 'john@example.com')
loan_book(1, 1, '2024-01-15')
List Records

python
Copy code
print('Books in the library:')
for book in list_books():
    print(book)

print('\nBorrowers:')
for borrower in list_borrowers():
    print(borrower)

print('\nLoans:')
for loan in list_loans():
    print(loan)


# License
This project is licensed under the MIT License. See the LICENSE file for details.

For any issues or suggestions, please contact the project maintainer.







