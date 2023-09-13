# Solution 1

### SELECT IN SELECT
 
``` sql
SELECT contragent FROM bankrate 
WHERE contragent IN (SELECT contragent FROM bankrate 
WHERE typeraiting = 'GLOBAL' AND to_char(raitingdate, 'YYYY/MM/DD') LIKE '2023%') AND typeraiting = 'RU'
GROUP BY contragent;
```



# Solution 2

### SELECT in JOIN table with SELECT

``` sql
SELECT bankrate.contragent FROM bankrate 
INNER JOIN (SELECT contragent FROM bankrate 
WHERE typeraiting = 'GLOBAL' AND to_char(raitingdate, 'YYYY/MM/DD') LIKE '2023%') AS a ON a.contragent = bankrate.contragent 
WHERE typeraiting = 'RU' AND to_char(raitingdate, 'YYYY/MM/DD') LIKE '2023%';
```
