# Task_first_SQL
create the schema and table. colum and  constraint
//Customer Table

CREATE Table Customer(
    Customer_id number(5)primary key,
    First_Name varchar2(20) Not Null ,
    Last_name Varchar2(20)Not Null,
    Email varchar2(30) Not null unique,
    mobile_no varchar2(25),
    Customer_Address varchar2(50),
    username varchar2(25),
    city varchar2(20),
    State varchar2(20)
);

// Products Table

CREATE Table Products(
    Product_id number(10) primary key,
    produst_Name varchar2(50) Not Null,
    price number(10)Not null,
    Discription  clob,
    Quantity number(10) Not Null,
    Category Varchar2(10)
);

// Order Table

create Table Orders(
    order_id number(10 )primary key,
    Customer_id number(10) constraint Customer_id_for references Customer(Customer_id),
    order_date date default sysdate,
    total_amount number(10,2) not null,
    status varchar2(15)
);



describe Customer;


describe Orders;
