# JavaScript Expert - TDD

## 📌 Project Overview
This project implements a car rental system using **Test-Driven Development (TDD)** with **Mocha**, **Chai**, and **Sinon** for testing. It follows a structured development approach, ensuring code reliability and maintainability.

## ✨ Features
- **Random Car Selection**: Selects a random available car from a category.
- **Price Calculation**: Computes the final rental price, including age-based tax.
- **Transaction Management**: Generates rental transactions with customer, car, price, and due date information.

## 🛠️ Technologies Used
- **JavaScript (Node.js)**
- **Mocha** - Test framework
- **Chai** - Assertion library
- **Sinon** - Mocks and spies for testing

## 📂 Project Structure
```
📦 javascript-expert--tdd
├── 📂 database          # JSON database for cars, categories, and customers
├── 📂 seed              # Data seeding scripts
├── 📂 src               # Application source code
│   ├── 📂 entities      # Business logic entities (Car, Customer, etc.)
│   ├── 📂 repository    # Data access layer
│   ├── 📂 service       # Business logic (CarService)
├── 📂 test              # Unit tests
│   ├── 📂 mocks         # Mock data for tests
│   ├── 📂 unitTests     # Test suite
│   ├── 📂 useCases      # Use case definitions
├── 📜 .nycrc.json       # Test coverage config
├── 📜 package.json      # Project dependencies
├── 📜 README.md         # Documentation
```

## Use Cases
### **Use Case 01 - Find an Available Car**
- Given a car category with three different cars
- When a user checks for availability
- Then the system selects a random car from the chosen category

### **Use Case 02 - Calculate Rental Price**
- Given a customer aged 50 renting a car for 5 days
- When selecting a car category costing $37.6/day
- Then the final price is calculated with a 30% age tax
- Final formula: `((price per day * Tax) * number of days) = $244.40`

### **Use Case 03 - Register a Rental Transaction**
- Given a 50-year-old customer renting a car for 5 days
- When renting a $37.6/day car
- Then the transaction includes:
  - Customer details
  - Selected car
  - Final price: **R$ 244,40**
  - Due date formatted as: **10 de Novembro de 2020**

## 🚀 Installation & Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/willyoliv/javascript-expert--tdd.git
   cd javascript-expert--tdd
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Run tests:
   ```sh
   npm test
   ```
4. Run tests with coverage:
   ```sh
   npm run test:cov
   ```
