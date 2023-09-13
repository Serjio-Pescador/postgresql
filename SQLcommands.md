## Create database for checking

```sql

CREATE TABLE bankrate (
    contragent     varchar(50),
    typeraiting    varchar(6),
    raitingdate    date,
    rating         varchar(8)
);

INSERT INTO bankrate (contragent, typeraiting, raitingdate, rating) VALUES
('VTB bank', 'RU', '2021-03-28', 'AA+(rus)'),
('VTB bank', 'RU','2023-05-02','BB(rus)'),
('VTB bank', 'GLOBAL','2023-05-02','ВВВ-'),
('Alfa-Bank', 'RU','2021-06-17','AA-(RU)'),
('Alfa-Bank', 'GLOBAL','2020-06-21','Ba1');

INSERT INTO bankrate (contragent, typeraiting, raitingdate, rating) VALUES
('Alfa-Bank', 'RU','2023-03-03','BB-(RU)'),
('Alfa-Bank', 'GLOBAL','2023-05-15','АА-'),
('Raiffeisenbank', 'RU','2021-12-17','CCC(RU)'),
('Raiffeisenbank', 'RU','2022-12-17','BBB(RU)'),
('Raiffeisenbank', 'RU','2023-12-17','AAA(RU)');

INSERT INTO bankrate (contragent, typeraiting, raitingdate, rating) VALUES
('UniCredit Bank AG', 'DE','2023-01-12','Baa3'),
('UniCredit Bank AG', 'DE','2023-02-25','Baa3'),
('UniCredit Bank AG', 'GLOBAL','2023-02-25','ВВВ+'),
('Bank of China', 'CN','2023-02-18','A2'),
('Bank of China', 'GLOBAL','2023-03-11','A1');

INSERT INTO bankrate (contragent, typeraiting, raitingdate, rating) VALUES
('Bank VTB Kazakhstan', 'KZ','2021-11-04','BB+'),
('Bank VTB Kazakhstan', 'KZ','2022-03-27','BB+'),
('City bank', 'RU','2021-08-09','A(RU)'),
('City bank', 'RU','2022-08-09','A(RU)'),
('City bank', 'RU','2023-08-09','A(RU)');

select * from bankrate;
```
