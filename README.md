# Customer Complaint Management System (CCMS) - Search Customer Page

This repository contains the PHP code for the "Search Customer" functionality in the Customer Complaint Management System (CCMS). The code allows authenticated users to search for customers by their ID or name and view details or complaints associated with the customer.

## Table of Contents

- [Prerequisites](#prerequisites)
- [File Structure](#file-structure)
- [How It Works](#how-it-works)
- [Styling](#styling)
- [JavaScript](#javascript)
- [Security](#security)
- [Known Issues](#known-issues)
- [Contact](#contact)

## Prerequisites

- PHP 7.x or higher
- MySQL Database
- A web server like Apache or Nginx
- Basic understanding of HTML, CSS, and PHP

## File Structure

- `search_customer.php`: The main PHP file that handles the search functionality.
- `dbconnection.php`: Includes the database connection settings.
- `sidebar&header.php`: Contains the code for the sidebar and header.
- `footer.php`: Contains the code for the footer.
- `style.css`: Includes the CSS used for styling the page.

## How It Works

1. **Session Management**: The code starts with a session check to ensure that the user is logged in and is authorized to access the page. The user type is checked to allow access only to a specific type of user.

2. **Search Functionality**: 
   - The user can search for customers by entering either the customer's ID or name in the search input field.
   - Upon submission, the form sends the search query to the server via POST.
   - The server queries the `user_detail` table to fetch records that match the search criteria.
   - If records are found, they are displayed in a table with options to view details or complaints related to each customer.

3. **Styling**:
   - The page is styled using a combination of inline CSS and external styles to ensure a consistent and visually appealing user interface.
   - The colors and styles are selected to provide a professional and user-friendly experience.

4. **JavaScript**:
   - A small JavaScript snippet is included to handle the sidebar toggle functionality. This allows users to expand or collapse the sidebar as needed.

5. **Security**:
   - Basic session management is used to ensure that only authenticated and authorized users can access the page.
   - Input from the search form is sanitized before being used in SQL queries to prevent SQL injection attacks.

## Styling

The page is styled using inline CSS. The main components include:

- **Main Content**: The main content area shifts based on the sidebar's width.
- **Footer**: The footer is positioned at the bottom of the page.
- **Table**: The search results are displayed in a responsive, striped table with alternating colors for rows.

## JavaScript

A JavaScript function is included to manage the sidebar's toggle functionality, allowing users to expand or collapse the sidebar.

## Security

- **Session Management**: Users must be logged in and have the correct user type (`user_type_id = 2`) to access this page.
- **SQL Queries**: Input from the search form is used in a query to search the `user_detail` table, with proper escaping of variables to prevent SQL injection.

## Known Issues

- The code currently does not handle empty search results gracefully. If a user searches for a non-existing customer, a generic "No records found" message is displayed.
- There is no pagination implemented, so a large number of search results could lead to long page load times.

## Contact

For any questions, issues, or suggestions, please contact the developer at [zakishah2k2@gmail.com](mailto:zakishah2k2@gmail.com).

