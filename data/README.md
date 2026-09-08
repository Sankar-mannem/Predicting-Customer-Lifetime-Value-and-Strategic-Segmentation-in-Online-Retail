# Data

This project uses the **Online Retail II** transactional dataset.

The dataset contains historical online retail transactions, including:

- Invoice information
- Product/Stock Code
- Product Description
- Quantity
- Invoice Date
- Unit Price
- Customer ID
- Country

## Data Source

The dataset is based on the Online Retail II dataset.

The raw dataset is not included in this repository because of file size and distribution considerations.

To reproduce the analysis, download the dataset separately and place the Excel file in the appropriate local data directory.

## Data Preparation

The analysis combines the:

- `Year 2009-2010`
- `Year 2010-2011`

sheets.

The data is then cleaned by:

1. Removing duplicate records
2. Removing transactions without Customer ID
3. Removing cancelled invoices
4. Removing non-positive quantities
5. Removing non-positive prices
6. Creating `TotalPrice = Quantity × Price`
7. Converting `InvoiceDate` to datetime format

The cleaned transaction data is then used to create customer-level behavioural features for CLV prediction and customer segmentation.
