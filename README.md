# My_SQLite_Library_Database
All my library books inserted manually to a SQLite database library

# My SQLite Library Database

Welcome to the **My SQLite Library Database** repository! This project is dedicated to managing a personal library database using SQLite, providing an efficient way to organize and manage book collections.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Database Schema](#database-schema)
6. [Contributing](#contributing)
7. [License](#license)

---

## Project Overview

This SQLite-based project aims to help users organize their personal library by:

- Storing book details such as title, author, genre, and publication year.
- Tracking borrowed books and their return dates.
- Uploading reviews to platforms like Goodreads.
- Providing a user-friendly interface for database operations.

## Features

- **CRUD Operations:** Easily create, read, update, and delete book records.
- **Search Functionality:** Search books by title, author, or genre.
- **Borrowed Book Tracker:** Manage borrowed books and set return reminders.
- **Integration:** Export and upload book reviews to Goodreads.
- **Statistics:** Generate reports on reading habits and book genres.

## Installation

### Prerequisites

- Python 3.7+
- SQLite (comes pre-installed with Python)

### Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/OYanez85/My_SQLite_Library_Database.git
   ```

2. Navigate to the project directory:

   ```bash
   cd My_SQLite_Library_Database
   ```

3. Install required dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Run the application:

   ```bash
   python main.py
   ```

## Usage

### Adding a New Book

1. Open the application.
2. Select the option to add a new book.
3. Fill in the required details such as title, author, genre, and publication year.

### Searching for Books

1. Use the search functionality to look up books by title, author, or genre.
2. Filter results as needed.

### Borrowed Books

1. Mark books as borrowed and specify the borrower and return date.
2. View borrowed books in a separate list with due dates.

### Export Reviews

1. Generate reviews for selected books.
2. Export the reviews in a format compatible with Goodreads.

## Database Schema

The database is designed with the following schema:

### Tables:

1. **Books**:
   - `id` (INTEGER PRIMARY KEY)
   - `title` (TEXT)
   - `author` (TEXT)
   - `genre` (TEXT)
   - `publication_year` (INTEGER)

2. **BorrowedBooks**:
   - `id` (INTEGER PRIMARY KEY)
   - `book_id` (INTEGER, FOREIGN KEY referencing Books.id)
   - `borrower` (TEXT)
   - `return_date` (DATE)

3. **Reviews**:
   - `id` (INTEGER PRIMARY KEY)
   - `book_id` (INTEGER, FOREIGN KEY referencing Books.id)
   - `review` (TEXT)

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature:

   ```bash
   git checkout -b feature-name
   ```

3. Commit your changes:

   ```bash
   git commit -m "Add feature description"
   ```

4. Push your changes:

   ```bash
   git push origin feature-name
   ```

5. Submit a pull request.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---

Thank you for checking out the My SQLite Library Database! If you have any questions or suggestions, feel free to open an issue or reach out.

