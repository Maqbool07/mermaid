erDiagram
  -- Entities
  CUSTOMER ||--o{ ORDER : places
  CUSTOMER ||--o{ INVOICE : "creates"
  ORDER ||--o{ ORDER_ITEM : "contains"
  PRODUCT ||--o{ ORDER_ITEM : "is in"

  -- Attributes
  CUSTOMER {
    +ID: INT
    Name: STRING
    Email: STRING
  }

  ORDER {
    +OrderID: INT
    OrderDate: DATE
  }

  INVOICE {
    +InvoiceID: INT
    Amount: FLOAT
  }

  ORDER_ITEM {
    +OrderItemID: INT
    Quantity: INT
    Price: FLOAT
  }

  PRODUCT {
    +ProductID: INT
    ProductName: STRING
  }


