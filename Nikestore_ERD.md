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
