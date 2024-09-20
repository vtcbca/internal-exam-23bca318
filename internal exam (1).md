Create table cricketer(cid, cname, match, run) and insert 8 players records. Print player records with average. and write this data into player.csv file. Do all this task from python


```python
import csv
```


```python
import sqlite3 as sq
```


```python
con=sq.connect("D:/23bca318/sqlite3/cricket.db")
```


```python
c=con.cursor()
```

CREATE TABLE


```python
c.execute("create table if not exists cricketer(cid,cname,matches,run)")
```




    <sqlite3.Cursor at 0x1ef971a8500>




```python
c.execute("insert into cricketer values(1,'virat',30,19000),(2,'hardik',21,32000),(3,'gill',13,4000),(4,'rohit',24,6000),(5,'raj',55,55000),(6,'dhoni',45,3800),(7,'rahul',16,7000),(8,'pratham',51,6500)")
```




    <sqlite3.Cursor at 0x1ef971a8500>



 PRINT  PLAYERS RECORDS WITH 


```python
c.execute("select * ,run/matches as average from cricketer")
rows=c.fetchall()
for row in rows:
    print(row)
    
```

    (1, 'virat', 30, 19000, 633)
    (2, 'hardik', 21, 32000, 1523)
    (3, 'gill', 13, 4000, 307)
    (4, 'rohit', 24, 6000, 250)
    (5, 'raj', 55, 55000, 1000)
    (6, 'dhoni', 45, 3800, 84)
    (7, 'rahul', 16, 7000, 437)
    (8, 'pratham', 51, 6500, 127)
    


```python

```
