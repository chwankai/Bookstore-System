# Teeple K Bookstore System 📚

A comprehensive, console-based Book Store Management System built in C++. This project was developed to demonstrate Object-Oriented Programming (OOP) concepts, file handling, algorithmic sorting/searching, and dynamic data structures (Linked Lists) in a practical application.

## 🚀 Features

The system supports two distinct user roles with dedicated functionalities:

### 🛒 Customer Module
* **User Authentication:** Secure registration and login functionality.
* **Browse & Search:** View all available books or search using Binary Search (by Book ID, Title, or Author).
* **Sort Catalog:** Sort books using Insertion Sort for easier browsing.
* **Shopping Cart:** Add items to the cart, edit quantities, and remove items.
* **Checkout System:** Process orders, calculate totals, automatically update inventory stock, and generate receipts.
* **Order Management:** Track order status, view order history, and search specific past orders using Jump Search.
* **Profile Management:** Safely update account passwords.

### 🛠️ Admin Module
* **Inventory Management:** Add new books, update existing book information, and delete obsolete books from the system.
* **Order Fulfillment:** View customer orders, inspect order details (including customer contact info), and update delivery statuses (Preparing, Delivered, Cancelled).
* **Sales Reporting:** Generate comprehensive reports to calculate total costs, earnings, and profits based on sold stock.
* **Admin Management:** Register new administrator accounts to the system.
* **Catalog Control:** Full access to search and sort both the entire book inventory and the global order database.

## 🧠 Technical Highlights
* **Object-Oriented Programming (OOP):** Utilizes inheritance, polymorphism, and abstract classes (e.g., base classes `USERS` and `BOOK` inherited by `CUST`, `ADMIN`, `CBOOK`, and `ABOOK`).
* **Data Structures:** Implements **Linked Lists** to handle dynamic, in-memory data for users, books, orders, order details, and shopping carts.
* **Algorithms:**
  * **Searching:** Binary Search (for locating books) and Jump Search (for locating orders).
  * **Sorting:** Insertion Sort (used for sorting IDs, Titles, Authors, Usernames, and Order Statuses).
* **Persistent Storage:** File-based I/O database system using standard text files.

## 📁 File Database Structure
The system relies on several text files to act as a persistent database. *(Note: The program requires these files to read/write data).*
* `users.txt`: Stores customer and admin credentials, phone numbers, and addresses (Role 1 = Customer | Role 2 = Admin).
* `books.txt`: Stores book metadata, pricing, available stock, and sold stock.
* `orders.txt`: Stores global order summaries, grand totals, and current fulfillment statuses.
* `orderdetails.txt`: Stores the specific Product IDs and quantities for each order.
* `cart.txt`: Stores active shopping cart states for all users.

## 💻 Getting Started

### Prerequisites
* A C++ compiler (e.g., GCC, MinGW, or an IDE like Dev-C++, Visual Studio, or Code::Blocks).
* Windows Environment (The code utilizes `system("CLS")` for UI rendering).

### Installation & Execution
1. Clone this repository to your local machine.
2. Ensure the `.cpp` source file and all text database files (`books.txt`, `users.txt`, `orders.txt`, `orderdetails.txt`, `cart.txt`) are located in the same directory. *(If starting fresh, create empty `.txt` files with these exact names).*
3. Compile the program using your terminal or IDE:
```bash
g++ bookstore_system.cpp -o bookstore
```
4. Run the executable:
```bash
./bookstore
```
