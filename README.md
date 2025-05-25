# repair-and-payment-system
This Entity-Relationship Diagram (ERD) represents a repair and payment system for managing customers, computers, repairs, and associated transactions. The entities and relationships are as follows: 

CUSTOMERS: Includes attributes like CustomerID (primary key), LastName, FirstName, Email, Htel, and Mobile. A customer can own multiple COMPUTERS (1:N) and request multiple REPAIRJOBS (1:1).
COMPUTERS: Contains attributes such as ComputerID (primary key), SerialNum, Make, and Model. A computer is owned by one CUSTOMER (1:1) and can be associated with multiple REPAIRJOBS (1:N).
REPAIRJOBS: Has attributes like JobNum (primary key), DateReceived, DateReturned, DateEnded, LaborCost, and TotalCost. A REPAIRJOB is requested by one CUSTOMER (1:1), performed on one COMPUTER (1:1), uses multiple ITEMS (0:N), and is conducted by one REPAIRMEN (1:N). A REPAIRJOB can also make multiple PAYMENTS (0:N).
REPAIRMEN: Includes attributes such as RepairmenID (primary key), LastName, FirstName, Extension, and Mobile. A repairman can perform multiple REPAIRJOBS (1:N).
ITEMS: Contains attributes like ItemID (primary key), PartNum, ShortName, Cost, and NumInStock. Items can be used in multiple REPAIRJOBS (0:N) and are ordered in multiple ORDERS (0:N).
ORDERS: Has attributes like OrderID (primary key). An order is associated with multiple ITEMS (0:N) and can have multiple DEPOSITS (0:N).
DEPOSITS: Includes attributes such as DepositNum (primary key), DepositDate, and Amount. A deposit is linked to one ORDER (1:1).
PAYMENTS: Contains attributes like PaymentNum (primary key), PaymentDate, and Amount. A payment is made for one REPAIRJOB (1:1).
# Relationships:

A CUSTOMER owns multiple COMPUTERS and requests REPAIRJOBS.
A COMPUTER is owned by one CUSTOMER and associated with REPAIRJOBS.
A REPAIRJOB is requested by a CUSTOMER, performed on a COMPUTER, uses ITEMS, is conducted by a REPAIRMEN, and makes PAYMENTS.
A REPAIRMEN performs multiple REPAIRJOBS.
ITEMS are used in REPAIRJOBS and ordered in ORDERS.
An ORDER is linked to ITEMS and DEPOSITS.
A DEPOSIT is associated with one ORDER.
A PAYMENT is linked to one REPAIRJOB.
The ERD uses diamonds to represent relationships (e.g., "own," "request," "use," "perform," "make," "order," "conducted") and ovals/rectangles for attributes and entities, with primary keys underlined and multiplicities (e.g., 0:N, 1:1) indicating cardinality.
