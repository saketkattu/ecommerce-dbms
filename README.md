# ecommerce-dbms
A ecommerce application that demonstrates the functioning of DBMS.
Semester 6 DBMS Project by Saket Kattuboina (RA1911031010107), K Easha Nair (RA1911031010110) and Apoorvi Singh (RA1911031010106).


### Database Implementation
#### Creating Tables 

```
CREATE TABLE products (
  id INT PRIMARY KEY,
  name VARCHAR(40) NOT NULL,
  price INT NOT NULL,
  quantity_remaining INT NOT NULL,
  image VARCHAR(300),
  weight DECIMAL,
  sku VARCHAR(20)
  
  );

CREATE TABLE `order`(
  id INT PRIMARY KEY ,
  cust_name VARCHAR(40) NOT NULL,
  shipping_add VARCHAR(100) NOT NULL,
  order_date DATE,
  total_weight DECIMAL,
  product_id INT,
  FOREIGN KEY(cust_name) REFERENCES customers(name),
  FOREIGN KEY(product_id) REFERENCES products(id)
  );
  
 
CREATE TABLE customers(
  name VARCHAR(40) PRIMARY KEY,
  email VARCHAR(40) NOT NULL,
  phone VARCHAR(10) NOT NULL,
  address VARCHAR(100) NOT NULL,
  payment_method VARCHAR(100)
  
  );



