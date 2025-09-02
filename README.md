# Audit-data-cleaning

## Audit Dataset (Accounts Receivable)
![img alt](https://github.com/nsankareswari-70/Audit-data-cleaning/blob/9894901e84e56386c19cfaf8dac1d7268a9c6bc1/audit1.png)

## Common Issues in the Raw Data
- Inconsistent Formats(dates in YYYY-MM-DD, DD/MM/YYYY, DD-MM-YYYY)
- Inconsistent text (ABC Ltd vs abc limited, inconsistent casing in Region/Currency)
- Missing values (NULLs in Customer_Name, Payment_Date, Invoice_Amount)
- Negative or Invalid values (Invoice_Amount=-1500)
- Duplicates (INV001 and INV002 look like duplicates for the same customer, same amount)
- Outliers (1.2 M transaction is a huge number compare to other entries. Need to be verified.)
  
