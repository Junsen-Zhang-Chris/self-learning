# self-learning




## LEVEL A:

Create database  + name + ; ==  Create a randomly named database.
Show database;              ==   Search all databases on your desktop and display them.
Select database();          ==  Search the database which you are using right now and display it.
Use + database’s name + ;   ==   Select out the database which you want to use.
Drop database + name + ;    ==   Delete the database. 


Create table + name + (.....)  +; == Create your table in the database.
Int == The numbers that need to be filled in the form are integers.
Varchar(x) ==  The number of words you fill in here is less than x.
Decs + table’s name + ;           ==  Query the structure of your custom table.





Alter table + table’s name + (rename) + new name + ； ==  Change the table’s name.
Eg.We can also change the command in () except ‘rename’ such as, ‘modify’, ’change’, ’drop’.
Drop table + table’s name + ;  ==  Delete the table.


Insert into +table’s name + values(.....) == Add information to the table.



Update + table’s name + set + xx=yy(where +condition) == change the table’s name from xx to yy in the condition of.....

We can also use “delete from” to replace the”update”  means delete xx from the table.



\\\\\\\\\\\\\\\\\\\





## LEVEL B:


### In the terminal and MySQL:

Create table products (
    id int auto_ increment primary key, 
    name varchar(255) not null,
    description text,
    price decimal(10, 2) not null,
    quantity int not null
);


### In python:

import mysql.connector

#connect to the database:
db = mysql.connector.connect(
  host="local",
  user="Chris",
  password="junsenzhang",
  database="inventory"）
)

   #create a cursor object:    
   cursor = db.cursor()

   #execute a query:    
   cursor.execute("SELECT * FROM products")

   #fetch all rows:    
   rows = cursor.fetchall()
   
   #close the database connection:    
   db.close()



### Using Flask:

#imports the Flask module and the render_template function from the Flask library, and the mysql.connector module:      
from flask import Flask, render_template
import mysql.connector

app = Flask(__name__)

@app.route('/')
def index():   
  
  db = mysql.connector.connect(
   host="local",
   user="Chris",
   password="junsenzhang",
   database="inventory"）
  )

    cursor = db.cursor()

    #execute a query to get all products:   
    cursor.execute("SELECT * FROM products")

    #fetch all rows:    
    rows = cursor.fetchall()

    db.close()

    #render the template with the product data:   
    return render_template('index.html', products=rows)




### Methods of adding or deleting:

@app.route('/add', methods=['POST'])
def add():
    
    #get form data:
    name = request.form['name']
    description = request.form['description']
    price = request.form['price']
    quantity = request.form['quantity']

    db = mysql.connector.connect(
      host="local",
      user="Chris",
      password="junsenzhang",
      database="inventory"
    )

    cursor = db.cursor()

    #execute a query to insert the new product:   
    cursor.execute("INSERT INTO products (name, description, price, quantity) VALUES (%s, %s, %s, %s)", (name, description, price, quantity))

    #commit the transaction:   
    db.commit()
    
    db.close()

    #redirect to the index page:     
    return redirect('/')


@app.route('/delete/<int:id>', methods=['POST'])
def delete(id):
    try:
        

\\\\\\\\\\\\\\\\\\\\\\\\\\

Firstly, i design an appropriate database schema to store and manage product data on the terminal:

Create table products (
    id int auto_ increment primary key, 
    name varchar(255) not null,
    description text,
    price decimal(10, 2) not null,
    quantity int not null
);

Secondly, to create my application, I choose Python as  programming language as it has a MySQL connector library that makes it easy to interact with a MySQL database. And then using the mysql-connector-python library to connect to my MySQL database and execute SQL queries:


Import  mysql.connector

db = mysql.connector.connect(
  host="local",
  user="Chris",
  password="junsenzhang",
  database="inventory"）

cursor = db.cursor()

cursor.execute("SELECT * FROM products")

rows = cursor.fetchall()

db.close()


Then, i create the user interface, by using the Flask:


from flask import Flask, render_template
import mysql.connector

app = Flask(__name__)

@app.route('/')
def index():
    
    db = mysql.connector.connect(
      host="local",
      user="Chris",
      password="junsenzhang",
      database="inventory"
)

    cursor = db.cursor()

    cursor.execute("SELECT * FROM products")

    rows = cursor.fetchall()

    db.close()

    return render_template('index.html', products=rows)




What’s more, there are also some methods to handle user input and validate user input to prevent errors and security vulnerabilities:

1. adding a new product:

@app.route('/add', methods=['POST'])
def add():
   
    name = request.form['name']
    description = request.form['description']
    price = request.form['price']
    quantity = request.form['quantity']

    db = mysql.connector.connect(
      host="local",
      user="Chris",
      password="junsenzhang",
      database="inventory"
    )

    cursor = db.cursor()

    cursor.execute("INSERT INTO products (name, description, price, quantity) VALUES (%s, %s, %s, %s)", (name, description, price, quantity))

    db.commit()

    db.close()

    return redirect('/')



2. deleting a product:


@app.route('/delete/<int:id>', methods=['POST'])
def delete(id):
    try:
      



