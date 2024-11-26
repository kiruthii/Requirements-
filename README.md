
# Bookstore Purchase System - JavaScript 

## Overview
This JavaScript function simulates a bookstore's purchase process, including removing duplicate books, applying discounts based on customer type, preparing a formatted bill, and updating the stock and customer details.

### Features:
- **Remove duplicates**: Remove duplicate book entries based on book ID.
- **Get customer’s chosen books**: Filter books based on customer selection.
- **Apply discounts**: Calculate discounts for new and existing customers based on the price of the books.
- **Prepare bill**: Generate a detailed bill with book titles, quantities, prices, discounts, and total.
- **Update stock**: Adjust stock quantities after purchase.
- **Update customer details**: Record the details of the last purchase made by the customer.


## Requirements

### Data
- **Books list**: A list of books, each with the following properties:
  - `id`: Unique identifier for the book.
  - `title`: Name of the book.
  - `price`: Price of the book in rupees.
  - `stock`: The number of books available in stock.

- **Customers list**: A list of customers, each with the following properties:
  - `id`: Unique identifier for the customer.
  - `name`: Name of the customer.
  - `isExistingCustomer`: Boolean indicating whether the customer is a returning customer.
  - `lastPurchase`: Details of the customer's last purchase (optional).


## Functionality

1. **RemoveDuplicates**:
   - Use a `Set` to eliminate duplicate books from the list based on the book's ID.

2. **GetCustomer’s Chosen Books**:
   - Filter the book inventory based on the provided list of book IDs.

3. **Calculate Discount**:
   - For **existing customers**, apply a 15% discount on books priced above ₹200.
   - For **new customers**, apply discounts based on the price range:
     - ₹100–₹200: 2%
     - ₹200–₹500: 5%
     - ₹500–₹750: 10%
     - Above ₹750: 15%

4. **Prepare Bill**:
   - Calculate the total price after applying discounts.
   - Include a breakdown of:
     - Book titles
     - Quantity
     - Individual prices before and after discount
     - Total price
     - Discount applied

5. **Update Stock**:
   - Reduce the stock count for each book purchased.

6. **Update Customer Details**:
   - Update the `lastPurchase` with details of the recent purchase, including:
     - Date of purchase
     - Books purchased
     - Total amount spent


## Technical Requirements

- Use **map** and **filter** for processing arrays.
- Use **Set** to remove duplicate book entries.
- Use **if...else** or **switch** for conditional discount logic.
- Use **objects** and **arrays** to organize data.
- Use operators (e.g., `+=`, `-=`) to handle stock updates and calculations.


## Output

The function should return an object with the following structure:

```javascript
{
  bill: {
    customerName: 'John Doe',
    booksPurchased: [
      { title: 'Book A', quantity: 1, price: 300, discount: 45, finalPrice: 255 },
      { title: 'Book B', quantity: 1, price: 150, discount: 3, finalPrice: 147 }
    ],
    totalPrice: 402,
    totalDiscount: 48
  },
  updatedStock: [
    { id: 1, title: 'Book A', stock: 9 },
    { id: 2, title: 'Book B', stock: 3 }
  ],
  updatedCustomerDetails: {
    id: 101,
    name: 'John Doe',
    isExistingCustomer: true,
    lastPurchase: {
      date: '2024-11-26',
      booksPurchased: ['Book A', 'Book B'],
      totalAmount: 402
    }
  }
}
```



## Sample Execution

### Input:
```javascript
const bookIds = [1, 2, 2, 3];  // Books chosen by the customer
const customerId = 101;        // Customer making the purchase
```

### Output:
```javascript
{
  bill: {
    customerName: 'John Doe',
    booksPurchased: [
      { title: 'Book A', quantity: 1, price: 300, discount: 45, finalPrice: 255 },
      { title: 'Book B', quantity: 1, price: 150, discount: 3, finalPrice: 147 }
    ],
    totalPrice: 402,
    totalDiscount: 48
  },
  updatedStock: [
    { id: 1, title: 'Book A', stock: 9 },
    { id: 2, title: 'Book B', stock: 3 }
  ],
  updatedCustomerDetails: {
    id: 101,
    name: 'John Doe',
    isExistingCustomer: true,
    lastPurchase: {
      date: '2024-11-26',
      booksPurchased: ['Book A', 'Book B'],
      totalAmount: 402
    }
  }
}









