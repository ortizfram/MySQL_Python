# MySQL_Python
## importing data bases in python 
🌟 here the link to my **SQL cheatsheet** 👇

https://github.com/ortizfram/MySQL-cheatsheet

🔗 thes scripts used for examples 👇

(most of them from first folder)

https://bit.ly/3rvtqdO


🧮 import, connect , and choose database
```
import mysql.connector

midb = mysql.connector.connect(
    host= 'localhost',
    user= 'root',
    password = '*********',
    database = 'sql_store'
)
```
ℹ️`cursor` used to interact with the DataBase using SQL 

ℹ️`execute()` inside this goes QUERYS

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

cursor.execute(sql, values)

```
- commit changes :
```
midb.commit()
```
