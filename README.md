# NikeStore_ERD.md
 
erDiagram
    PRODUCT {
        string product_id PK
        string product_name
        string size
        string color
        decimal price
    }
    CUSTOMER {
        string customer_id PK
        string first_name
        string last_name
        string email
        string phone
    }
    SALE {
        string sale_id PK
        string customer_id FK
        string product_id FK
        date sale_date
        decimal sale_amount
    }
    INVENTORY {
        string product_id FK
        int stock_quantity
    }

    CUSTOMER ||--o| SALE : makes
    PRODUCT ||--o| SALE : sold_in
    PRODUCT ||--o| INVENTORY : has_stock
