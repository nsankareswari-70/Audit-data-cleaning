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
  
## Data Cleaning Process
### Step 1: Highlight Blanks and Missing values
Highlight all the blank cells and Fill it with N/A

### Step 2: 
Replace all the 'limited' with 'Ltd' to maintain consistency
Replace abc with ABC
Remove all the . with nothing

### Step 3:
To make the Invoice_Date column format constistant - change to date(dd,mm,yyyy) format
=TEXT(C2,"dd-mm-yyyy")

### Step 4:
Mark the negative values highlight it with Red. Used conditonal formating to highlight the cells with the value < 0

### Step 5:
Highlight the outlier value. Invoice amount 12000000 look like a outlier mark it with different colour for later verification

### Step 6:
Replace all the $ sign in the currency sign with 'USD' 
Replace all the usd with 'USD'

### Step 7:
Make the case as proper for the Region column
=proper(h2)

### Final cleaned Data
![img alt](https://github.com/nsankareswari-70/Audit-data-cleaning/blob/cac04d7a6ec4059601c91f13c756038aabbb2a6f/audit2.png)
