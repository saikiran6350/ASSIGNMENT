# ASSIGNMENT
MariaDB [(none)]> use information;
Database changed
MariaDB [information]> create table employees(empid int(5),empname varchar(30),empbranch varchar(15),empdesignation varchar(40),ampaddr varchar(100),empcontn_no int(10),primary key(empid));
ERROR 1050 (42S01): Table 'employees' already exists
MariaDB [information]> desc employees;
+----------------+--------------+------+-----+---------+-------+
| Field          | Type         | Null | Key | Default | Extra |
+----------------+--------------+------+-----+---------+-------+
| empid          | int(5)       | NO   | PRI | NULL    |       |                                                            1ST TABLE ABOUT EMPLOYEES
| empname        | varchar(30)  | YES  |     | NULL    |       |
| empbranch      | varchar(15)  | YES  |     | NULL    |       |
| empdesignation | varchar(40)  | YES  |     | NULL    |       |
| ampaddr        | varchar(100) | YES  |     | NULL    |       |
| empcontn_no    | int(10)      | YES  |     | NULL    |       |
+----------------+--------------+------+-----+---------+-------+
6 rows in set (0.021 sec)

MariaDB [information]> insert into employees values(1045,'hari','hyderabad','acountant','hyderabad',9873457623);
Query OK, 1 row affected, 1 warning (0.005 sec)
insert into employees values(1012,'naresh','pune','assistantmaneger','chennai',8976562310);
Query OK, 1 row affected, 1 warning (0.006 sec)

MariaDB [information]> insert into employees values(1032,'nani','chennai','manager','vizag',9347390009);
Query OK, 1 row affected, 1 warning (0.006 sec)

MariaDB [information]> insert into employees values(1022,'lokesh','delhi','manager','delhi',8897028349);
Query OK, 1 row affected, 1 warning (0.005 sec)

MariaDB [information]> select*from employees;                                           
+-------+----------+-----------+------------------+-----------+-------------+
| empid | empname  | empbranch | empdesignation   | ampaddr   | empcontn_no |
+-------+----------+-----------+------------------+-----------+-------------+
|  1002 | ganesh   | vizag     | manager          | hyderabad |  2147483647 |
|  1004 | haribabu | hyderabad | accountant       | hyderabad |  2147483647 |          
|  1012 | naresh   | pune      | assistantmaneger | chennai   |  2147483647 |
|  1022 | lokesh   | delhi     | manager          | delhi     |  2147483647 |
|  1032 | nani     | chennai   | manager          | vizag     |  2147483647 |
|  1045 | hari     | hyderabad | acountant        | hyderabad |  2147483647 |
+-------+----------+-----------+------------------+-----------+-------------+
6 rows in set (0.000 sec)
MariaDB [information]> create table customer(cust_id int(4),cust_name varchar(30),cust_emailid varchar(50),cust_contno int(10),membership_id int,primary key(cust_id));
Query OK, 0 rows affected (0.073 sec)








MariaDB [information]> create table membership(m_id int,start_date text,end_date text,primary key(m_id));
Query OK, 0 rows affected (0.045 sec)

MariaDB [information]> desc membership;
+------------+---------+------+-----+---------+-------+
| Field      | Type    | Null | Key | Default | Extra |
+------------+---------+------+-----+---------+-------+                                                                   2nd TABLE ABOUT MEMBERSHIP
| m_id       | int(11) | NO   | PRI | NULL    |       |
| start_date | text    | YES  |     | NULL    |       |
| end_date   | text    | YES  |     | NULL    |       |
+------------+---------+------+-----+---------+-------+
3 rows in set (0.029 sec)
MariaDB [information]> insert into membership values(10034,20-6-2023,19-6-2024);
Query OK, 1 row affected (0.005 sec)

MariaDB [information]> insert into membership values(10244,26-3-2023,25-3-2025);
Query OK, 1 row affected (0.004 sec)

MariaDB [information]> insert into membership values(10346,26-3-2021,25-3-2025);
Query OK, 1 row affected (0.004 sec)

MariaDB [information]> insert into membership values(10354,26-3-2023,25-3-2029);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> select*from membership;
+-------+------------+----------+
| m_id  | start_date | end_date |
+-------+------------+----------+
| 10034 | -2009      | -2011    |
| 10244 | -2000      | -2003    |
| 10346 | -1998      | -2003    |
| 10354 | -2000      | -2007    |
+-------+------------+----------+
4 rows in set (0.000 sec)















MariaDB [information]> desc customer;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |
+---------------+-------------+------+-----+---------+-------+
| cust_id       | int(4)      | NO   | PRI | NULL    |       |
| cust_name     | varchar(30) | YES  |     | NULL    |       |                                                     3rd TABLE  ABOUT CUSTOMER
| cust_emailid  | varchar(50) | YES  |     | NULL    |       |
| cust_contno   | int(10)     | YES  |     | NULL    |       |
| membership_id | int(11)     | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
5 rows in set (0.026 sec)

MariaDB [information]> insert into customer values
    -> ();
Query OK, 1 row affected, 1 warning (0.006 sec)

MariaDB [information]> insert into customer values(10023,'haribabu','haribabu2@gmail.com',9347303008,4110);
Query OK, 1 row affected, 1 warning (0.006 sec)

MariaDB [information]> insert into customer values(10122,'nandakishore','nanda30@gmail.com',8897018934,4121);
Query OK, 1 row affected, 1 warning (0.005 sec)
MariaDB [information]> insert into customer values(10054,'nani','nani78@gmail.com',9382048229,4129);
Query OK, 1 row affected, 1 warning (0.006 sec)

MariaDB [information]> insert into customer values(10069,'sai','sai09@gmail.com',9874328760,4132);
Query OK, 1 row affected, 1 warning (0.005 sec)

MariaDB [information]> select*from customer;
+---------+--------------+---------------------+-------------+---------------+
| cust_id | cust_name    | cust_emailid        | cust_contno | membership_id |
+---------+--------------+---------------------+-------------+---------------+
|       0 | NULL         | NULL                |        NULL |          NULL |
|   10023 | haribabu     | haribabu2@gmail.com |  2147483647 |          4110 |
|   10054 | nani         | nani78@gmail.com    |  2147483647 |          4129 |
|   10069 | sai          | sai09@gmail.com     |  2147483647 |          4132 |
|   10122 | nandakishore | nanda30@gmail.com   |  2147483647 |          4121 |
+---------+--------------+---------------------+-------------+---------------+
5 rows in set (0.000 sec)







MariaDB [information]> create table shipment(sdcontent varchar(40),sddomain varchar(15),sdtype varchar(15),sdweight varchar(10),sdcharges int(10),customerid int(4),primary key(customerid));
Query OK, 0 rows affected (0.122 sec)

MariaDB [information]> desc shipment;
+------------+-------------+------+-----+---------+-------+
| Field      | Type        | Null | Key | Default | Extra |
+------------+-------------+------+-----+---------+-------+
| sdcontent  | varchar(40) | YES  |     | NULL    |       |                                                                   5th TABLE ABOUT SHIPMENT
| sddomain   | varchar(15) | YES  |     | NULL    |       |
| sdtype     | varchar(15) | YES  |     | NULL    |       |
| sdweight   | varchar(10) | YES  |     | NULL    |       |
| sdcharges  | int(10)     | YES  |     | NULL    |       |
| customerid | int(4)      | NO   | PRI | NULL    |       |
+------------+-------------+------+-----+---------+-------+
6 rows in set (0.045 sec)

MariaDB [information]> create table shipment2(sdid int(10),sdaddr varchar(100),dsaddr varchar(100),customerid int(4),primary key(sdid),foreign key(customerid) references shipment(customerid));
Query OK, 0 rows affected (0.051 sec)

MariaDB [information]> desc shipment2;
+------------+--------------+------+-----+---------+-------+
| Field      | Type         | Null | Key | Default | Extra |
+------------+--------------+------+-----+---------+-------+
| sdid       | int(10)      | NO   | PRI | NULL    |       |
| sdaddr     | varchar(100) | YES  |     | NULL    |       |
| dsaddr     | varchar(100) | YES  |     | NULL    |       |
| customerid | int(4)       | YES  | MUL | NULL    |       |
+------------+--------------+------+-----+---------+-------+
4 rows in set (0.027 sec)

MariaDB [information]> insert into shipment values('cloths','domestic','regular','fiftytons','10000',1002);
Query OK, 1 row affected (0.009 sec)

MariaDB [information]> insert into shipment values('snacks','domestic','regular','oneton','15000',1232);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into shipment values('sweets','domestic','regular','oneton','20000',1312);
Query OK, 1 row affected (0.004 sec)

MariaDB [information]> insert into shipment values('oilpackets','domestic','express','fiftytons','55000',1312);
ERROR 1062 (23000): Duplicate entry '1312' for key 'PRIMARY'
MariaDB [information]> insert into shipment values('oilpackets','domestic','express','fiftytons','55000',1442);
Query OK, 1 row affected (0.004 sec)
MariaDB [information]> select*from shipment;
+------------+----------+---------+-----------+-----------+------------+
| sdcontent  | sddomain | sdtype  | sdweight  | sdcharges | customerid |
+------------+----------+---------+-----------+-----------+------------+
| cloths     | domestic | regular | fiftytons |     10000 |       1002 |
| snacks     | domestic | regular | oneton    |     15000 |       1232 |
| sweets     | domestic | regular | oneton    |     20000 |       1312 |
| oilpackets | domestic | express | fiftytons |     55000 |       1442 |
+------------+----------+---------+-----------+-----------+------------+
4 rows in set (0.007 sec)
MariaDB [information]> insert into shipment2 values(41110,'chennai','vizag',1002);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into shipment2 values(41132,'chennai','banglore',1232);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into shipment2 values(41212,'vizag','bombay',1442);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into shipment2 values(41244,'pune','tiruvananthapuram',1312);
Query OK, 1 row affected (0.004 sec)

MariaDB [information]> select*from shipment2;
+-------+---------+-------------------+------------+
| sdid  | sdaddr  | dsaddr            | customerid |
+-------+---------+-------------------+------------+
| 41110 | chennai | vizag             |       1002 |
| 41132 | chennai | banglore          |       1232 |
| 41212 | vizag   | bombay            |       1442 |
| 41244 | pune    | tiruvananthapuram |       1312 |
+-------+---------+-------------------+------------+
4 rows in set (0.000 sec)









MariaDB [information]> create table status(shid varchar(6),current_st varchar(15),sent_date text,delivery_date text,primary key(sh_id));
ERROR 1072 (42000): Key column 'sh_id' doesn't exist in table
MariaDB [information]> create table status(shid varchar(6),current_st varchar(15),sent_date text,delivery_date text,primary key(shid));
Query OK, 0 rows affected (0.083 sec)

MariaDB [information]> desc status;
+---------------+-------------+------+-----+---------+-------+
| Field         | Type        | Null | Key | Default | Extra |                                                          6th TABLE ABOUT STATUS
+---------------+-------------+------+-----+---------+-------+
| shid          | varchar(6)  | NO   | PRI | NULL    |       |
| current_st    | varchar(15) | YES  |     | NULL    |       |
| sent_date     | text        | YES  |     | NULL    |       |
| delivery_date | text        | YES  |     | NULL    |       |
+---------------+-------------+------+-----+---------+-------+
4 rows in set (0.029 sec)

MariaDB [information]> insert into status values('three','ready_to_ship',20-6-2023,23-6-2023);
Query OK, 1 row affected (0.005 sec)

MariaDB [information]> insert into status values('six','delivered',18-6-2023,21-6-2023);
Query OK, 1 row affected (0.002 sec)

MariaDB [information]> insert into status values('four','delivered',19-6-2023,19-6-2023);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into status values('nine','shippingcompleted',19-6-2023,23-6-2023);
Query OK, 1 row affected, 1 warning (0.003 sec)

MariaDB [information]> insert into status values('one','delivered',19-6-2023,22-6-2023);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into status values('ten','shipped',19-6-2023,25-6-2023);
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> select*from status;
+-------+-----------------+-----------+---------------+
| shid  | current_st      | sent_date | delivery_date |
+-------+-----------------+-----------+---------------+
| four  | delivered       | -2010     | -2010         |
| nine  | shippingcomplet | -2010     | -2006         |
| one   | delivered       | -2010     | -2007         |
| six   | delivered       | -2011     | -2008         |
| ten   | shipped         | -2010     | -2004         |
| three | ready_to_ship   | -2009     | -2006         |
+-------+-----------------+-----------+---------------+
6 rows in set (0.000 sec)













MariaDB [information]> create table relation(employee_id int(5),sdid int(10),shid varchar(6),foreign key(shid) references status(shid));
Query OK, 0 rows affected (0.032 sec)

MariaDB [information]> desc relation;
+-------------+------------+------+-----+---------+-------+
| Field       | Type       | Null | Key | Default | Extra |                                           7th TABLE ABOUT RELATION B/W SHIPMENT AND STATUS
+-------------+------------+------+-----+---------+-------+
| employee_id | int(5)     | YES  |     | NULL    |       |
| sdid        | int(10)    | YES  |     | NULL    |       |
| shid        | varchar(6) | YES  | MUL | NULL    |       |
+-------------+------------+------+-----+---------+-------+
3 rows in set (0.026 sec)

MariaDB [information]> insert into relation values(1002,41132,'three');
Query OK, 1 row affected (0.004 sec)

MariaDB [information]> insert into relation values(1022,41212,'nine');
Query OK, 1 row affected (0.003 sec)

MariaDB [information]> insert into relation values(1032,41244,'four');
Query OK, 1 row affected (0.002 sec)

MariaDB [information]> insert into relation values(1022,41110,'one');
Query OK, 1 row affected (0.004 sec)

MariaDB [information]> select*from relation;
+-------------+-------+-------+
| employee_id | sdid  | shid  |
+-------------+-------+-------+
|        1002 | 41132 | three |
|        1022 | 41212 | nine  |
|        1032 | 41244 | four  |
|        1022 | 41110 | one   |
+-------------+-------+-------+
4 rows in set (0.000 sec)

