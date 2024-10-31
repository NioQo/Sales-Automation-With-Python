# Profit-Report-Automation-With-Python

# Abstract
Tisagar is a cryptocurrency arbitrageur, trading on multiple exchanges to maximize his profits. Each month, Tisagar must declare its profits, which requires daily tracking of transactions across exchanges. However, he faces a significant challenge: each exchange offers a different format for downloading transactions, which complicates the daily recording process. This effort consumes approximately 20 hours per month to complete the Excel required for reporting.
![image](https://github.com/user-attachments/assets/31d02db2-4a08-4474-946b-e02a722a26d8)



# Introduce
In this project, we work with data from eight cryptocurrency exchanges to automate a monthly profit report
- Binance
- BinanceSpot
- Fiwind
- Bybit
- Bitget
- OKX
- Bitso
- Lemon


# Objective
The goal of this project is to automate the process of collecting and formatting transaction data, reducing the time spent and improving efficiency in information management.


# Data Preparation
## Steps for Each Exchange
### Fiwind 
- Remove rows where "monto origen" is blank.
- Delete unnecessary columns: 'Tipo,' 'Moneda Origen,' 'Moneda,' 'Precio.'
- Create a calculated column: "precio."
- Add constant columns with values: Exchange Venta, Banco Recibido.
- Reorder columns as required.
- Insert a blank row after each day's data.
### Bybit 
- Remove unnecessary columns: 'p2p-convert,' 'Currency,' 'cryptocurrency,' 'Transaction Fees,' 'Counterparty,' 'Status.'
- Separate data into two tables by transaction type: "sell" and "buy."
- Insert a blank row after each day's data.
- Arrange columns for both tables in the correct order.
- Export tables.
### Binance
### Sell Transactions 
- Remove unnecessary columns: 'Order type,' 'Fiat Type,' 'Exchange rate,' 'Maker fee,' 'Maker Fee Rate,' 'Taker Fee,' 'Taker Fee rate,' 'Counterparty,' 'Status.'
- Create a column: Exchange Venta = "Binance - [Asset Type]."
- Add constant column: Banco Recibo = "Lemon."
- Reorder columns as specified.
- Insert a blank row after each day's data.
- Export table
### Buy Transactions 
- Remove unnecessary columns: 'Order Type,' 'Fiat Type,' 'Exchange rate,' 'Maker Fee,' 'Maker Fee Rate,' 'Taker Fee,' 'Taker Fee rate,' 'Counterparty,' 'Status.'
- Create a column: Exchange Compra = "Binance - [Asset Type]."
- Add constant column: Banco Envio = "Lemon."
- Perform calculation per day:
  - Calculating the daily average "usdt."
  - Setting "Price" to the daily average if Asset Type is BTC or ETH.
  - Calculating "Quantity" as Total Price / Price.
- Reorder columns as needed.
- Insert a blank row after each day's data.
- Export table.

The same data preparation steps, including column deletions, additions of constant columns, and daily blank row insertions, are applied to other exchanges as needed.
# Result

We have achieved an impressive transformation in our data management. By unifying all transactions into a single Excel file, we have drastically reduced the time required to complete the benefits reporting process. We went from **20 hours per month** to just **2 hours per month**. Not only does this represent a **90% reduction in work time**, but it has also allowed for greater efficiency and accuracy in tracking transactions.

Importantly, although we continue to deal with exchanges that do not offer the option to download transactions, requiring manual entry and daily calculation of profits, the automation of the other processes has freed up valuable time that was previously spent on tedious tasks.
