 ```mermaid
erDiagram
PRODUCT ||--|{ SALE : for
PRODUCT {
    string serialnumber
}
CUSTOMER ||--o{ PRODUCT : Buys
CUSTOMER {
    string name
    string cardnumber  
}
SALE ||--|{ INVENTORY : Changes
SALE { 
    string serialnumber
    string cardnumber
} 
INVENTORY ||--|{ PRODUCT : Order
INVENTORY {
    string serialnumber
}
CUSTOMER ||--o{ SALE : info
```
Documentation:
 Products are the shoes that the store is selling to the customer.
 The customer is purchacing the shoes through a sale by giving their card number.
 The sale moves product out of the store deplenting inventory.
 Inventory is increased to keep products in the store for customers to buy.

 These relationships are important because when one of these four categories fails the whole store suffers. For example, if you dont keep your inventory up you won't have enough products for the customers. Keeping track of the sales of the products with serial numbers can help you see which shoes you need to oder more or less of. 
