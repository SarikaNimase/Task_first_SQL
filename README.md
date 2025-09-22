<img width="1920" height="1080" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/57dd369e-529f-48ed-b12e-ceda0b2ffd47" /># Task_first_SQL
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

#output

<img width="1920" height="1080" alt="Screenshot (5)" src="https://github.com/user-attachments/assets/681ec1fc-4175-4754-b3bb-78ace9d84cdc" />
<img width="1920" height="1080" alt="Screenshot (6)" src="https://github.com/user-attachments/assets/2ddb7a02-b4b4-4fcb-9b36-30ff115b87ae" />
<img width="1920" height="1080" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/f6c26f5c-3dfe-4219-becc-e9fb660f180a" />
<img width="1920" height="1080" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/da0ff8fd-c658-46fb-bfe3-dfc9542fdfd2" />
<img width="1920" height="1080" alt="Screenshot (9)" src="https://github.com/user-attachments/assets/98b6794e-b043-490a-8301-193201fd3015" />
<img width="1920" height="1080" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/970cfcb3-6752-430c-90cd-2f3d85c64f96" />
<img width="1920" height="1080" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/46d51588-cc0e-41fb-9654-0a6b61ae70c8" />

# ER Daigram


<img width="1536" height="1024" alt="ER_ daigram" src="https://github.com/user-attachments/assets/7ec2b438-b042-424e-b872-36487c9752ba" />
