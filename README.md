# MySQL_Python
## importing data bases in python 
đ here the link to my **SQL cheatsheet** đ

https://github.com/ortizfram/MySQL-cheatsheet

đ thes scripts used for examples đ

(most of them from first folder)

https://bit.ly/3rvtqdO


đ§Ž import, connect , and choose database
```
import mysql.connector

midb = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password = '*********',
    database = 'sql_store'
)
```
âšī¸`cursor` used to interact with the DataBase using SQL 

âšī¸`execute()` inside this goes QUERYS

- fetchall : gives all results found

- fetchone : gives only the first result

then you print with an alias assigned to fetchall
```
cursor = midb.cursor()
cursor.execute('select * from customers')
result = cursor.fetchall()
print(result)
```

## entering new data

```
sql = 'INSERT INTO customers(phone, first_name, city) values (%s, %s, %s)'
values = ('1234566', 'franco', 'MDZ')
cursor.EXECUTE(sql, values)

resultado = cursor.fetchall()
print(resultado)
```
- commit changes :
```
midb.commit()
```
- affected rows :
```
print(cursor.rowcount)
```

