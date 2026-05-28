# Customer Data Modeling and Deduplication

This project is based on Chapter 3 of *The Well-Grounded Data Analyst*.  
The goal is to build a clean customer data model from multiple raw data sources and create a more reliable estimate of the customer base.

## Project Goal

The business question is:

**Who are our customers?**

To answer this, I combined customer information from three sources:

- Purchase transaction data
- CRM export data
- Customer database data

The final output is a customer data model that makes it easier to count unique customers and understand where each customer record came from.

## Datasets Used

The analysis uses three datasets:

- `purchases.csv`
- `crm_export.csv`
- `customer_database.csv`

The purchase data includes both registered customers and guest checkout customers.  
The CRM and customer database files contain customer details such as name, surname, postcode, and age.

## Main Steps

1. Loaded and inspected the datasets
2. Checked missing values and basic data quality issues
3. Identified guest and non-guest purchases
4. Extracted customer details from purchase data
5. Standardized column names across all datasets
6. Combined purchase, CRM, and customer database records
7. Added source-tracking columns, such as:
   - `is_guest`
   - `in_purchase_data`
   - `in_crm_data`
   - `in_customer_data`
8. Cleaned text fields by standardizing capitalization and removing extra spaces
9. Identified duplicate customer records
10. Used entity resolution logic to link likely duplicate customers

## Key Result

The final customer model provides a cleaner and more reliable view of the customer base.

In the chapter example, the combined dataset contained:

- 35,395 total customer records
- 27,394 unique or main customer records

This shows why data modeling is important: raw records are not always the same as real customers.

## Tools Used

- Python
- pandas
- NumPy
- recordlinkage
- Jupyter Notebook

## Skills Practiced

- Data cleaning
- Data modeling
- Combining multiple datasets
- Handling missing values
- Creating a common schema
- Deduplicating customer records
- Entity resolution
- Tracking data lineage
  

## Conclusion

This project shows how raw transactional and customer data can be transformed into a more useful customer data model.  
By combining, cleaning, and deduplicating records, the business can answer basic questions like customer count more accurately and reuse the model for future customer analysis.

## Project Source

This project is based on Chapter 3, **Data Modeling**, from *The Well-Grounded Data Analyst* by David Asboth.


## Author

**Sophie Ranj**

Data Analyst  
[Portfolio](https://sophie-ranj.github.io/)
