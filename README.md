- 👋 Hi, I’m @KeerthiPadagarla
- 👀 I’m interested in creating database,  ...
- 🌱 I’m currently doing my masters in computescience  ...
- 💞️ I’m looking to collaborate on development fileld ...
- 📫 How to reach me prabhakarkeerthi1971@gmail.com ...
-
<!---
KeerthiPadagarla/KeerthiPadagarla is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
#my work on creating database to store movies
#create database
import mysql.connector
import cgi
#create a new database______
dataBase = mysql.connector.connect(
    user='root',
    password='',
    host='localhost')

#prepare a cursor object_____
cur = dataBase.cursor()

#create new "films" database_____
cur.execute("CREATE DATABASE films;")
print("films - database created succesfully")
cur.close()
dataBase.close()      
#creation of table using python 
import mysql.connector
import cgi
#create a new database______
con = mysql.connector.connect(
    user='root',
    password='',
    database='films',
    host='localhost')
   

#create cursor _____
cur = con.cursor()

#Insert data into "moive" table___
n=int(input('enter how many Movies:'))
for i in range(n):
    print('enter ',i+1,'Movies Details')
    mov_name=input('Movie Name:')
    act_name=input('Actor Name:')
    actrs_name=input('Actress Name:')
    dir_name=input('Director Name:')
    res_date=input('Release Date:')
   
cur.execute("insert into movies values(%s, %s, %s, %s, %s)",
            (mov_name, act_name, actrs_name, dir_name, res_date))
con.commit()

print("data inserted into MOVIES TABLE succesfully")
cur.close()
con.close()      
#insertion of data into sql through python
import mysql.connector
import cgi
#create a new database______
con = mysql.connector.connect(
    user='root',
    password='',
    database='films',
    host='localhost')
   

#prepare a cursor object_____
cur = con.cursor()

#create new "movies" TABLE_____
TableName = "CREATE TABLE movies(name VARCHAR(30),actor VARCHAR(30),actress VARCHAR(30),director VARCHAR(30),releasedate DATE );"
#execute cursor     
cur.execute(TableName)
print("movies - tablecreated succesfully")
cur.close()
dataBase.close()    
[image](https://user-images.githubusercontent.com/99889213/155851383-2e4de9c1-b947-41a8-b2fb-446b9f6f4e93.png)
[image](https://user-images.githubusercontent.com/99889213/155851395-25ec5ce8-a822-42fb-a808-4be0a928ce66.png)
http://localhost/phpmyadmin/index.php?route=/sql&server=1&db=films&table=movies&pos=0
[movies .pdf](https://github.com/KeerthiPadagarla/KeerthiPadagarla/files/8147044/movies.pdf)


    
