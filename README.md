# 🌟 **Expense Tracker**  
### _A Personal Finance Management Tool_ 🌟

Welcome to **Expense Tracker**, a sleek and powerful desktop application designed to help you manage your personal expenses with ease. Developed using **Java** and **PostgreSQL**, this application features an intuitive user interface powered by **JavaFX**, allowing you to track, filter, and manage your financial records efficiently.

---

## 📋 **Project Overview**

**Expense Tracker** offers a simple yet powerful way to manage your finances. With this app, you can:

- **Add Expenses**: Record expense details like description, amount, category, and date.
- **View All Expenses**: Display all recorded expenses in a structured and organized format.
- **Filter Data**: Easily filter expenses by **month** or **category**.
- **Update Expenses**: Modify existing records to ensure accuracy.
- **Delete Expenses**: Remove specific records or clear all data at once.

This app is designed for both beginners and experienced users, simplifying personal finance management with a clean, responsive interface.

---

## 🚀 **Features**

- **Add Expenses**: Input details such as description, amount, category, and date for each expense.
- **View All Expenses**: See all expenses displayed in a clear and user-friendly table.
- **Filter Data**:
  - **By Month**: Filter expenses by a specific month (e.g., `2024-12`).
  - **By Category**: Filter by categories such as **Food**, **Transport**, **Entertainment**, etc.
- **Update Expenses**: Modify any expense record (description, amount, category).
- **Delete Expenses**: Delete specific records or remove all records from the database with a single click.

---

## 🛠 **Technologies Used**

- **Programming Language**: Java (Version 11 or higher)
- **UI Framework**: JavaFX for a modern, responsive interface
- **Database**: PostgreSQL for efficient data storage
- **Integration**: JDBC to facilitate seamless communication with the database

---

## 📝 **Setup Guide**

### 1️⃣ **Prerequisites**

Before running the project, ensure the following are installed:

- **JDK** (Java Development Kit): Version 11 or higher
- **PostgreSQL**: For managing the database
- **IDE**: IntelliJ IDEA, Eclipse, or any Java IDE of your choice

---

### 2️⃣ **Database Configuration**

1. **Create the Database**: Open PostgreSQL and create a new database:

    ```sql
    CREATE DATABASE expense_tracker;
    ```

2. **Run SQL Script**: Execute the provided `setup.sql` script to:
    - Create the necessary tables (`expenses`, `categories`).
    - Populate the `categories` table with sample data.

3. **Verify Tables**: Ensure the following tables are created:
    - `categories`: Stores predefined expense categories.
    - `expenses`: Stores detailed records of user expenses.

---

### 3️⃣ **Application Configuration**

1. Open the `DatabaseConnection.java` file.
2. Update the following database connection details with your credentials:

    ```java
    private static final String URL = "jdbc:postgresql://localhost:5432/expense_tracker";
    private static final String USER = "your_username";
    private static final String PASSWORD = "your_password";
    ```

---

### 4️⃣ **Running the Application**

1. Import the project into your IDE.
2. Open the `HelloApplication.java` file.
3. Run the `main` method to launch the application.

---

## ⚙️ **Usage Instructions**

### **1. Add an Expense**

1. Enter the following details:
   - **Description**: A brief note (e.g., "Coffee").
   - **Amount**: Numeric value (e.g., "5.00").
   - **Category**: Select from predefined categories (e.g., "Food").
   - **Date**: Format: `YYYY-MM-DD` (e.g., "2024-12-23").
   
2. Click **"Add Expense"** to save the record.

---

### **2. View All Expenses**

1. Click **"View All Expenses"** to display all recorded expenses in a structured table.

---

### **3. Filter Expenses**

1. **By Month**: Enter the month in `YYYY-MM` format (e.g., `2024-12`) and click **"Filter by Month"**.
2. **By Category**: Select a category from the dropdown and click **"Filter by Category"**.

---

### **4. Update an Expense**

1. Enter the **description** of the expense you want to update.
2. Modify any field (amount, category, etc.).
3. Click **"Update Expense"** to save the changes.

---

### **5. Delete an Expense**

1. **Specific Record**: Enter the description and click **"Delete Expense by Description"**.
2. **All Records**: Click **"Delete All Expenses"** to remove all records from the database.

---

## 📂 **Project Structure**

```plaintext
src/
├── org.example.expensetracker/
│   ├── DatabaseConnection.java   # Manages database connections
│   ├── Expense.java              # Expense model class
│   ├── ExpenseDAO.java           # CRUD operations for expenses
│   ├── HelloController.java      # Controls UI logic
│   ├── HelloApplication.java     # Main entry point for the application
│   └── resources/
│       ├── hello-view.fxml       # FXML layout for the user interface
│       └── expense-tracker.jpg   # Background image for the UI
└── setup.sql                     # SQL script to set up the database

