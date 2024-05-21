CREATE DATABASE SALES_MANAGEMENT_SYSTEM;
use SALES_MANAGEMENT_SYSTEM;

CREATE TABLE SALES_TRANSACTION(
Transaction_ID INT primary key not null,
Transaction_date date not null,
Customer_iD int, foreign key (customer_iD) references customer_information(customer_id),
Product_ID int, foreign key (product_id)references production_details(product_id),
Quantity_sold INT not null,
Total_amount INT not null);

CREATE TABLE Customer_Information(
Customer_iD INT primary key not null,
Name varchar(50) not null,
Email varchar(50) not null,
Address varchar(50) not null);

CREATE TABLE Production_details(
Product_ID INT primary key not null ,
Name varchar(50) not null,
Category varchar(50) not null,
Price int not null);

INSERT INTO SALES_TRANSACTION values
(1011, '2023-07-13', 9031, 45678, 3, 9000),
(1012, '2023-04-02', 9030, 56789, 2, 7000),
(1013, '2023-05-18', 9029, 678910, 5, 15000),
(1014, '2023-05-25', 9028, 7891011, 2, 7000),
(1015, '2023-06-07', 9027, 89101112, 3, 9000),
(1016, '2023-06-09', 9026, 9101113, 1, 3000),
(1017, '2023-08-02', 9025, 10111214, 4, 12000),
(1018, '2023-04-01', 9024,  11121314,5, 5000),
(1019, '2023-04-28', 9023, 12131415, 3, 9000),
(1020, '2023-01-29', 9022, 13141516, 2, 7000),
(1021, '2023-06-20', 9021, 14151617, 2, 7000),
(1022, '2023-05-19', 9020, 15161718, 2, 7000),
(1023, '2023-03-15', 9018, 19202122, 2, 7000),
(1024, '2023-02-10', 9019, 20212223, 4, 12000);

INSERT INTO Customer_Information values
(9018, 'Joshua Clinton', 'clinton@yahoo.com', '20, goriola street'),
(9019, 'Chioma Jesus', 'ilovejesus@yahoo.com', '30 mtn street'),
(9020, 'Moses Bliss', 'Bliss@gmail.com', '01 muritala close'),
(9021, 'Forrest Frank', 'frankfor@yahoo.com', '202 mohammed road'),
(9022, 'Caleb Gordon', 'unusualgordy@yahoo.com', '19 abeokuta street'),
(9023, 'Mary Saint', 'saints58@yahoo.com', '14 onabanjo street'),
(9024, 'Emeka Okafor', 'okae22@yahoo.com', '52 olabisi road'),
(9025, 'Diana Emelie', 'diane1@gmail.com', '10 ruphus street'),
(9026, 'Joshua Freeman', 'Freejosh43@yahoo.com', '09 joseph street'),
(9027, 'Ebuka Johnson', 'ebujames20@gmail.com', '11 olawale street'),
(9028, 'Omowunmi Michael', 'OMOMI@gmail.com', '27 akpabio street'),
(9029, 'Christabel Idemili', 'christyy@yahoo.com', '14 ude street'),
(9030, 'Olamide Joseph', 'olamide1@yahoo.com', '15 mount street'),
(9031, 'Favour Akinwale', 'favak123@gmail.com', '18 monica street');

INSERT INTO Production_details values
(45678, 'Custard', 'Baby food', 3000),
(56789, 'Diapers', 'Baby Item', 3500),
(678910, 'Mathematical set', 'Stationeries', 5000),
(7891011, 'Milo', 'Beverages', 3500),
(89101112, 'Nescafe', 'Beverages', 3000),
(9101113, 'Bag', 'Fashion', 3000),
(10111214, 'Milk', 'Baby food', 3000),
(11121314, 'Baby socks', 'Baby Item', 1000),
(12131415, 'Pen', 'Stationeries', 3000),
(13141516, 'Fruit Juice', 'Beverages', 3500),
(14151617, 'Feeding bottle', 'Baby Item', 3500),
(15161718, 'Notebook', 'Stationeries', 3500),
(19202122, 'Baby cloth', 'Baby item', 3500),
(20212223, 'pencil', 'stationeries', 3000);


-- 1 Adding a new sales transaction to the system 
Insert into SALES_TRANSACTION values
(1025, '2023-08-04', 9031, 20212223, 4, 12000);

-- 2 Updating the product associated with a sales transaction
Update Sales_Transaction
SET PRODUCT_ID = 56789
where Transaction_id = 1012;

-- 3 recording customer details for a sales transaction
Insert into customer_information values
(9032, 'Mabel Sarowiwa', 'mabsa402@gmail.com', '25 Easton street');

-- 4 Finding the total number of sales transaction for each product category
select Category, count(category) as total_num_of_trans from sales_transaction
join production_details 
on sales_transaction.Product_ID = production_details.Product_ID
group by category;

-- 5 retrieving the names of customers who made purchase in a specific month
select Name, Transaction_date from customer_information
join sales_transaction
on customer_information.customer_id = sales_transaction.customer_id
where transaction_date between '2023-06-01' and '2023-06-30';











