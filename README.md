# mysql
mysql

Logowanie do mysql


mysql> show databases;
+--------------------+
| Database           |
+--------------------+
| information_schema |
| kompart_main       |
+--------------------+
2 rows in set (0.02 sec)

Database changed
mysql> show tables;
+----------------------------+
| Tables_in_kompart_main     |
+----------------------------+
| kompart_abonenci           |
| kompart_abonenci_platnosci |
| kompart_cennikwydruk       |
| kompart_errlog             |
| kompart_komis              |
| kompart_menu               |
| kompart_newsy              |
| kompart_pilka              |
| kompart_podstrony          |
| kompart_zmienne            |
+----------------------------+
10 rows in set (0.00 sec)
mysql> describe kompart_abonenci;
+---------------------------+---------------------+------+-----+---------+----------------+
| Field                     | Type                | Null | Key | Default | Extra          |
+---------------------------+---------------------+------+-----+---------+----------------+
| id                        | int(11)             | NO   | PRI | NULL    | auto_increment |
| ip                        | varchar(15)         | NO   |     | NULL    |                |
| mac                       | varchar(17)         | YES  |     | NULL    |                |
| ip_zewn                   | varchar(15)         | NO   |     | NULL    |                |
| abonent                   | text                | NO   |     | NULL    |                |
| id_na_serwerze            | text                | NO   |     | NULL    |                |
| rodzaj_polaczenia         | int(11)             | NO   |     | NULL    |                |
| predkosc                  | int(11)             | NO   |     | NULL    |                |
| messageType               | tinyint(3) unsigned | YES  |     | 0       |                |
| messageCommon             | tinyint(3) unsigned | YES  |     | 0       |                |
| messageOther              | varchar(255)        | YES  |     | NULL    |                |
| niestandardowa_cena_lacza | double              | NO   |     | NULL    |                |
| rodzaj_sprzetu            | int(11)             | NO   |     | NULL    |                |
| rodzaj_sprzetu_inna       | text                | NO   |     | NULL    |                |
| rodzaj_anteny             | int(11)             | NO   |     | NULL    |                |
| rodzaj_anteny_inna        | text                | NO   |     | NULL    |                |
| kanal_wifi                | int(11)             | NO   |     | NULL    |                |
| kanal_wifi_inna           | text                | NO   |     | NULL    |                |
| wlasnosc_sprzetu          | int(11)             | NO   |     | NULL    |                |
| umowa_do                  | date                | NO   |     | NULL    |                |
| umowa_od                  | date                | NO   |     | NULL    |                |
| umowa_nieokreslona        | int(11)             | NO   |     | NULL    |                |
| opis                      | text                | NO   |     | NULL    |                |
| faktura_rodzaj            | int(11)             | NO   |     | NULL    |                |
| faktura_numer             | int(11)             | NO   |     | NULL    |                |
| sposob_zaplaty            | int(11)             | NO   |     | NULL    |                |
| adres                     | tinytext            | NO   |     | NULL    |                |
| telefon                   | tinytext            | NO   |     | NULL    |                |
| kod                       | varchar(100)        | NO   |     | NULL    |                |
| pesel                     | varchar(100)        | NO   |     | NULL    |                |
| email                     | varchar(100)        | NO   |     | NULL    |                |
| uwagi                     | text                | NO   |     | NULL    |                |
+---------------------------+---------------------+------+-----+---------+----------------+
32 rows in set (0.00 sec)
mysql>  ALTER TABLE kompart_komis ADD login_ppoe_1 VARCHAR(100) NOT NULL;
Query OK, 1 row affected (0.04 sec)
Records: 1  Duplicates: 0  Warnings: 0

mysql> describe kompart_komis;
+--------------+--------------+------+-----+---------+----------------+
| Field        | Type         | Null | Key | Default | Extra          |
+--------------+--------------+------+-----+---------+----------------+
| id           | int(11)      | NO   | PRI | NULL    | auto_increment |
| plik         | varchar(11)  | NO   |     | NULL    |                |
| nazwa        | text         | NO   |     | NULL    |                |
| opis         | text         | NO   |     | NULL    |                |
| cena         | varchar(10)  | NO   |     | NULL    |                |
| sztuki       | int(11)      | NO   |     | NULL    |                |
| wystaw       | int(11)      | NO   |     | NULL    |                |
| login_ppoe_1 | varchar(100) | NO   |     | NULL    |                |
+--------------+--------------+------+-----+---------+----------------+
8 rows in set (0.00 sec)

mysql>  ALTER TABLE kompart_komis DROP login_ppoe_1;
Query OK, 1 row affected (0.11 sec)
Records: 1  Duplicates: 0  Warnings: 0
