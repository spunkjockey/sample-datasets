# Retail Directoy Structure:

```
OrderDetail/
  00.csv
  01.csv
  02.csv
  04.csv
  05.csv
OrderDetail.zip
```

# Retail Details:

## OrderDetail/
- **format:** csv 
- **schema:**
```
root
 |-- ORDER_ID: string (nullable = true)
 |-- USER_ID: string (nullable = true)
 |-- ORDER_NUMBER: string (nullable = true)
 |-- ORDER_DOW: string (nullable = true)
 |-- ORDER_HOUR_OF_DAY: string (nullable = true)
 |-- DAYS_SINCE_PRIOR_ORDER: string (nullable = true)
 |-- ORDER_DETAIL: string (nullable = true)
```

## OrderDetail.zip
- **format:** parquet
- **schema:**
```
root
 |-- ORDER_ID: long (nullable = true)
 |-- USER_ID: long (nullable = true)
 |-- ORDER_NUMBER: short (nullable = true)
 |-- ORDER_HOUR_OF_DAY: short (nullable = true)
 |-- ORDER_DETAIL: array (nullable = true)
 |    |-- element: struct (containsNull = true)
 |    |    |-- PRODUCT: string (nullable = true)
 |    |    |-- AISLES: string (nullable = true)
 |    |    |-- PRODUCTS_SOLD: short (nullable = true)
 |-- ORDER_DOW: integer (nullable = true)
```
