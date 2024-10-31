# Sales-Automation-With-Python
 Profit Report Automation With Python
# Abstract
Tisagar is a cryptocurrency arbitrageur, trading on multiple exchanges to maximize his profits. Each month, Tisagar must declare its profits, which requires daily tracking of transactions across exchanges. However, he faces a significant challenge: each exchange offers a different format for downloading transactions, which complicates the daily recording process. This effort consumes approximately 20 hours per month to complete the Excel required for reporting.


# Introduce
In this project, we work with data from six cryptocurrency exchanges to automate a monthly profit report
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
### Steps for Each Exchange
Fiwind 
Remove rows where "monto origen" is blank.
Delete unnecessary columns: 'Tipo,' 'Moneda Origen,' 'Moneda,' 'Precio.'
Create a calculated column: "precio."
Add constant columns with values: Exchange Venta, Banco Recibido.
Reorder columns as required.
Insert a blank row after each day's data.
Bybit 
Remove unnecessary columns: 'p2p-convert,' 'Currency,' 'cryptocurrency,' 'Transaction Fees,' 'Counterparty,' 'Status.'
Separate data into two tables by transaction type: "sell" and "buy."
Insert a blank row after each day's data.
Arrange columns for both tables in the correct order.
Export tables.
Binance
Sell Transactions 
Remove unnecessary columns: 'Order type,' 'Fiat Type,' 'Exchange rate,' 'Maker fee,' 'Maker Fee Rate,' 'Taker Fee,' 'Taker Fee rate,' 'Counterparty,' 'Status.'
Create a column: Exchange Venta = "Binance - [Asset Type]."
Add constant column: Banco Recibo = "Lemon."
Reorder columns as specified.
Insert a blank row after each day's data.
Export table.
Buy Transactions 
Remove unnecessary columns: 'Order Type,' 'Fiat Type,' 'Exchange rate,' 'Maker Fee,' 'Maker Fee Rate,' 'Taker Fee,' 'Taker Fee rate,' 'Counterparty,' 'Status.'
Create a column: Exchange Compra = "Binance - [Asset Type]."
Add constant column: Banco Envio = "Lemon."
Perform the breakdown by:
Calculating the daily average "usdt."
Setting "Price" to the daily average if Asset Type is BTC or ETH.
Calculating "Quantity" as Total Price / Price.
Reorder columns as needed.
Insert a blank row after each day's data.
Export table.
The same data preparation steps, including column deletions, additions of constant columns, and daily blank row insertions, are applied to other exchanges as needed.


