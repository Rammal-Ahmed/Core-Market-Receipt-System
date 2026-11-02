# Core Market Receipt System

A Python-based supermarket billing application that processes customer purchases, applies eligible discounts, calculates shipping charges, and generates a detailed sales receipt.

Built as a practical Python project, it brings together fundamental programming concepts to handle a retail billing process from customer input to final payment.

---

## Overview

The Core Market Receipt System is a command-line application designed to simulate the billing process at a supermarket counter.

The program collects customer and product details, calculates the gross purchase amount, determines the applicable customer discount, checks eligibility for an additional card payment discount, and calculates shipping charges.

Once the billing process is complete, it generates a structured receipt displaying the purchase details, applied discounts, and total payable amount.

## Features

- Customer and product information input
- Automatic gross bill calculation
- Quantity-based customer classification
- VIP, Premium, and Regular customer discounts
- Additional card payment discount based on eligibility
- Conditional shipping charge calculation
- Automatic final payable amount calculation
- Formatted customer receipt
- Transaction completion message

---

## Billing Rules

The application follows predefined billing conditions to calculate discounts and shipping charges.

### 1. Purchase Discount

The customer category and discount rate are determined by the quantity purchased.

| Customer Category | Quantity | Discount |
|---|---:|---:|
| VIP Customer | 52 or above | 20% |
| Premium Customer | 35–51 | 10% |
| Regular Customer | 12–34 | 5% |
| Regular Customer | Below 12 | No Discount |

### 2. Card Payment Discount

An additional 25% discount on the original gross bill is available for card payments when either of the following conditions is met:

- The gross bill is Rs. 100,000 or above and the customer qualifies as a VIP customer.
- The gross bill is Rs. 200,000 or above, regardless of customer category.

Cash payments are not eligible for this additional discount.

### 3. Shipping Charges

Shipping charges are calculated using the final amount after applying the purchase and payment discounts.

| Final Amount | Shipping Charges |
|---|---:|
| Rs. 100,000 or above | Free Shipping |
| Rs. 50,000–99,999.99 | Rs. 250 |
| Below Rs. 50,000 | Rs. 500 |

---

## Technologies & Concepts

**Programming Language:** Python 3

**Core Concepts Used:**

- Variables and data types
- User input and type conversion (`int`, `float`)
- Conditional statements (`if`, `elif`, `else`)
- Compound conditional expressions (`and`, `or`)
- Arithmetic and percentage calculations
- String methods (`.lower()`, `.center()`)
- Console-based output formatting
- Implementation of conditional billing rules

No external Python libraries are required.

---

## Sample Run

### Customer Input

```text
What is your name, Sir?: Ahmed Khan
Which product would you like to purchase?: Cooking Oil (5L)
Product unit price (Rs.): 2400
What is the quantity, Sir?: 40
Enter payment method (Cash / Card): card
```

### Generated Receipt

```text
========================================
        CORE MARKET RECEIPT
       CUSTOMER SALES RECEIPT
========================================

Customer Name:           Ahmed Khan

Product Description:     Cooking Oil (5L)

Unit Price (Rs.):        2400.0

Quantity Purchased:      40

Gross Amount (Rs.):      96000.0

Purchase Discount (Rs.): 9600.0

Payment Discount (Rs.):  0

Net Amount (Rs.):        86400.0

Shipping Charges (Rs.):  250

Total Payable (Rs.):     86650.0

----------------------------------------
       TRANSACTION COMPLETED!
       THANK YOU FOR SHOPPING
    SEE YOU IN THE NEXT REPOSITORIES..!
========================================
```

**Note:** This example represents a Premium Customer purchase. Although the payment method is card, the purchase does not meet the additional card discount eligibility conditions.

---

## Getting Started

### Requirements

- Python 3
- A code editor or Python-compatible IDE
- No additional package installation required

### Installation & Execution

**1. Clone the repository**

```bash
git clone https://github.com/your-username/Core-Market-Receipt-System.git
```

**2. Navigate to the project directory**

```bash
cd Core-Market-Receipt-System
```

**3. Run the Python application**

```bash
python core_market_receipt_system.py
```

Follow the on-screen prompts to enter customer details, product information, quantity, and payment method.

---

## Project Structure

```text
Core-Market-Receipt-System/
│
├── core_market_receipt_system.py
├── CORE_MARKET_RECEIPT_SYSTEM.ipynb
├── README.md
└── LICENSE
```

---

## Learning Objectives

This project provided practical experience in applying Python fundamentals to a retail billing scenario.

The main focus was on:

- Translating business rules into conditional logic
- Handling different types of user input
- Working with multiple discount conditions
- Performing sequential billing calculations
- Understanding compound logical expressions
- Organizing console output for better readability

---

## Future Improvements

Potential enhancements to the application include:

- Supporting multiple products in a single transaction
- Adding input validation for prices, quantities, and payment methods
- Generating unique receipt numbers and transaction dates
- Saving customer receipts to text or CSV files
- Improving monetary formatting and receipt customization

---

## Author

**Your Name**

Microsoft Dynamics 365 CRM Developer | AI & Data Science Enthusiast

[LinkedIn] www.linkedin.com/in/rammal-ahmed-58184b325
[GitHub] https://github.com/Rammal-Ahmed

---

## License

This project is licensed under the **GNU Affero General Public License v3.0 (AGPL-3.0)**. See the [LICENSE](LICENSE) file for details.

---

**Project Status:** Completed
