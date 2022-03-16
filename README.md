# ecommerce-dbms
A ecommerce application that demonstrates the functioning of DBMS.
Semester 6 DBMS Project by Saket Kattuboina (RA1911031010107), K Easha Nair (RA1911031010110) and Apoorvi Singh (RA1911031010106).


### Database Implementation
#### Creating Tables 

```
CREATE TABLE Customer
    (
        Customer_id VARCHAR(6) NOT NULL,
        Name VARCHAR(20) NOT NULL,
        Address VARCHAR(20) NOT NULL,
        Pincode NUMBER(6) NOT NULL,
        Phone_number_s number(10) NOT NULL,
        PRIMARY KEY (Customer_id),
        
    );

CREATE TABLE Product
    (
        Product_id VARCHAR(7) NOT NULL,
        Type VARCHAR(7) NOT NULL,
        Color VARCHAR(15) NOT NULL,
        P_Size VARCHAR(2) NOT NULL,
        Cost NUMBER(5) NOT NULL,
        Quantity NUMBER(2) NOT NULL,
        Seller_id VARCHAR(6),
        PRIMARY KEY (Product_id),
    );
 
CREATE TABLE ORDERS 
(
       

);
```
