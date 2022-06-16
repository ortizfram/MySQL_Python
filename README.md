# MySQL_Python
## importing data bases in python 

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
ℹ️`fetchall()` gives results 
then you print with an alias assigned to fetchall
```
cursor = midb.cursor()

cursor.execute('select * from customers')

result = cursor.fetchall()

print(result)
```
