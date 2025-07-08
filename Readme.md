## 🧪 Sample Output

Here is the sample output of the program:

![Sample Output](images/output.png)

# 📚 Quantum Bookstore

## 📌 Project Overview

This Java project simulates an online bookstore system called **Quantum Bookstore**, supporting:

- Different types of books (paper books, ebooks, demo books).
- Interfaces for shipping and mailing services.
- Purchase process with validation.
- Handling of outdated (old) books.
- Encapsulated, extensible design using OOP.

---

## ⚙️ OOP Concepts Used

| Concept                  | Usage in Project                                                      |
|--------------------------|-----------------------------------------------------------------------|
| **Abstraction**           | `Book` abstract class, `ShippingService`, and `MailService` interfaces |
| **Inheritance**           | `PaperBook`, `EBook`, `ShowcaseBook` extend `Book`                   |
| **Polymorphism**          | Use of `Book` reference for all types                                |
| **Encapsulation**         | Fields are private/protected with validation in constructor          |
| **Interface Implementation** | `ConsoleShippingService`, `ConsoleMailService` implement service interfaces |

---

## 🧱 Class Summary

| Class/Interface            | Description                                                              |
|----------------------------|--------------------------------------------------------------------------|
| `Book`                     | Abstract base class for all book types                                   |
| `PaperBook`                | Represents a physical book, delivered via shipping                       |
| `EBook`                    | Represents a digital book, delivered via email                           |
| `ShowcaseBook`             | Not for sale, throws error when purchased                                |
| `ShippingService`          | Interface for shipping functionality                                     |
| `MailService`              | Interface for mailing functionality                                      |
| `ConsoleShippingService`   | Implementation of shipping (prints shipping info)                        |
| `ConsoleMailService`       | Implementation of mailing (prints email delivery info)                   |
| `Bookstore`                | Manages inventory, sales, and removal of outdated books                  |
| `QuantumBookstoreDemo`     | Main class with example test cases                                       |

---

## 🧪 Key Methods and Their Roles

### 🔹 `Book.java`
- `reduceStock(int qty)`: Reduces available quantity of the book.
- `isOutdated(int maxAge, int currentYear)`: Checks if a book is too old.
- `deliver(email, address)`: Abstract method to define how the book is delivered.

### 🔹 `PaperBook.java`
- Overrides `deliver()` to use shipping.

### 🔹 `EBook.java`
- Overrides `deliver()` to use mailing.

### 🔹 `ShowcaseBook.java`
- Overrides `deliver()` to throw an exception as it's not for sale.

### 🔹 `Bookstore.java`
- `addBook(Book book)`: Adds a book to inventory.
- `buyBook(String isbn, int quantity, String email, String address)`:
  - Validates availability and type.
  - Reduces stock.
  - Delivers book using appropriate service.
  - Calculates total cost and prints receipt.
- `removeOutdatedBooks(int maxAge)`: Removes old books based on year.

### 🔹 `QuantumBookstoreDemo.java`
- Tests the system by:
  - Attempting purchases.
  - Handling demo and unknown book errors.
  - Removing outdated books.

---



