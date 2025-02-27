mysql> create database invoice;
Query OK, 1 row affected (0.00 sec
mysql> use invoice;
Database changed
mysql> create table Customer(id int primary key, name varchar(10), address varcha
r(10), city varchar(10), ph_no double);
Query OK, 0 rows affected (0.01 sec)
ysql> desc Customer;
+---------+-------------+------+-----+---------+-------+
| Field   | Type        | Null | Key | Default | Extra |
+---------+-------------+------+-----+---------+-------+
| id      | int         | NO   | PRI | NULL    |       |
| name    | varchar(10) | YES  |     | NULL    |       |
| address | varchar(10) | YES  |     | NULL    |       |
| city    | varchar(10) | YES  |     | NULL    |       |
| ph_no   | double      | YES  |     | NULL    |       |
+---------+-------------+------+-----+---------+-------+
5 rows in set (0.00 sec)

mysql> create table Product (pid int primary key,pname varchar(20),price double default 0);
Query OK, 0 rows affected (0.01 sec)
mysql> desc Product;
+-------+-------------+------+-----+---------+-------+
| Field | Type        | Null | Key | Default | Extra |
+-------+-------------+------+-----+---------+-------+
| pid   | int         | NO   | PRI | NULL    |       |
| pname | varchar(20) | YES  |     | NULL    |       |
| price | double      | YES  |     | 0       |       |
+-------+-------------+------+-----+---------+-------+
mysql> create table Invoice_master(inv_id int primary key,cust_id int,inv_date date,foreign key (cust_id) references Customer(id));
Query OK, 0 rows affected (0.02 sec)
mysql> desc Invoice_master;
+----------+------+------+-----+---------+-------+
| Field    | Type | Null | Key | Default | Extra |
+----------+------+------+-----+---------+-------+
| inv_id   | int  | NO   | PRI | NULL    |       |
| cust_id  | int  | YES  | MUL | NULL    |       |
| inv_date | date | YES  |     | NULL    |       |
+----------+------+------+-----+---------+-------+
3 rows in set (0.00 sec)
mysql> create table Invoice_item (inv_id int,pid int,quantity double,foreign key(inv_id) references Invoice_master(inv_id),foreign key(pid) references Product(pid));
Query OK, 0 rows affected (0.01 sec)
mysql> desc Invoice_item;
+----------+--------+------+-----+---------+-------+
| Field    | Type   | Null | Key | Default | Extra |
+----------+--------+------+-----+---------+-------+
| inv_id   | int    | YES  | MUL | NULL    |       |
| pid      | int    | YES  | MUL | NULL    |       |
| quantity | double | YES  |     | NULL    |       |
+----------+--------+------+-----+---------+-------+
3 rows in set (0.00 sec)
//VERIFIED
