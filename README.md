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
        PRIMARY KEY (Customer_id)
        
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
        PRIMARY KEY (Product_id)
    );
 
CREATE TABLE ORDERS 
(
       Quantity_wished NUMBER(1) NOT NULL,
        Date_Added DATE NOT NULL,
        Cart_id VARCHAR(7) NOT NULL,
        Product_id VARCHAR(7) NOT NULL
        Purchased varchar(3)

);
CREATE TABLE Payment
    (
        payment_id VARCHAR(7) NOT NULL,
        payment_date DATE NOT NULL,
        Payment_type VARCHAR(10) NOT NULL,
        Customer_id VARCHAR(6) NOT NULL,
        Cart_id VARCHAR(7) NOT NULL,
        PRIMARY KEY (payment_id)
        total_amount numeric(6)
    );


***INSERTING VALUES

insert into Customer values('cid100','MAX','G-453','632014',9093137896);
insert into Customer values('cid101','LARA','G-567','632015',6593086543);
insert into Product values('pid1008','t-shirt','black',10,10007,10,'max100');
insert into Product values('pid2009','trousers','grey',18,49714,20,'lar100');
insert into ORDERS values(3,to_date('10-OCT-2021','dd-mon-yyyy'),'crt1091','pid1008','Y');
insert into ORDERS values(3,to_date('14-MAR-2021','dd-mon-yyyy'),'crt9051','pid2009','Y');
insert into Payment values('pmt1049',to_date('10-OCT-2021','dd-mon-yyyy'),'online','cid100','crt2011',NULL);
insert into Payment values('pmt2859',to_date('14-MAR-2021','dd-mon-yyyy'),'online','cid102','crt3011',NULL);
