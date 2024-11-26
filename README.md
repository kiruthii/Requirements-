# Requirements-
Requirements to Write the JavaScript Function
 1.
 2.
 Initialize Data:
 • Create alist of books with duplicates. Each book object
 should include:
 ❖id: A unique identifier for the book.
 ❖title: Name of the book.
 ❖price: Price of the book in rupees.
 ❖stock: The number of books available in stock.
 • Create alist of customers of the bookstore. Each customer
 object should include:
 ❖id: A unique identifier for the customer.
 ❖name:Nameofthe customer.
 ❖isExistingCustomer: Boolean indicating if they are a
 returning customer.
 ❖lastPurchase: Details of the last purchase (optional).
 Functionality:
 • RemoveDuplicates:
 Use a Set to remove duplicate entries from the book list based on the
 book’s id.
 • GetCustomer’s Chosen Books:
 Take a list of book ids as input and filter the books from the inventory
 based on the selection.
• Calculate Discount:
 • Forexisting customers:
 ➢Provide a 15% discount on books priced above ₹200.
 • Fornewcustomers:
 ➢Discount based on the price range:
 ➔₹100–₹200: 2%
 ➔₹200–₹500: 5%
 ➔₹500–₹750: 10%
 ➔Above₹750: 15%.
 • Prepare Bill:
 • Calculate the total price after applying the discount.
 • Includeabreakdown of the purchase:
 ❖Booktitles.
 ❖Quantity.
 ❖Individual prices before and after discount.
 ❖Total price.
 ❖Discount applied.
 • Formatthebill as an object.
 • UpdateStock:
 Reduce the stock count for each book purchased.
 • UpdateCustomer Details:
 Update the customer’s lastPurchase with details of the recent purchase,
 including the date, books purchased, and total amount.
 3.
 Technical Requirements:
• Usemapandfilter for processing arrays.
 • UseSettoeliminate duplicates.
 • Applyif...else or switch for conditional discount logic.
 • Useobjects and arrays for organizing data.
 • Utilize appropriate operators (+=,-=, etc.) to handle stock
 updates and calculations.
 4.
 Output:
 The function should return:
 • Aformatted bill object.
 • Updatedstock and customer details.
 5.
 Sample Execution:
 Input:
 const bookIds = [1, 2, 2, 3]; // Books chosen by the customer
 const customerId = 101; // Customer making the purchase
 Output:
 {
 bill: {
 customerName: 'John Doe',
 booksPurchased: [
 { title: 'Book A', quantity: 1, price: 300, discount: 45, finalPrice: 255 },
 { title: 'Book B', quantity: 1, price: 150, discount: 3, finalPrice: 147 }
 ],
 totalPrice: 402,
 totalDiscount: 48,
},
 }
 updatedStock: [...],
 updatedCustomerDetails: { ... },
