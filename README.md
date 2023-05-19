LaTeX:



\documentclass[a4paper, 11pt]{report}
\usepackage{blindtext}
\usepackage[T1]{fontenc}
\usepackage[utf8]{inputenc}
\usepackage{titlesec}
\usepackage{fancyhdr}
\usepackage{geometry}
\usepackage{fix-cm}
\usepackage[hidelinks]{hyperref}
\usepackage{graphicx}
\usepackage{titlesec}
\usepackage[english]{babel}
\usepackage{makecell}
\usepackage{float}

\geometry{ margin=30mm }
\counterwithin{subsection}{section}
\renewcommand\thesection{\arabic{section}.}
\renewcommand\thesubsection{\thesection\arabic{subsection}.}
\usepackage{tocloft}
\renewcommand{\cftchapleader}{\cftdotfill{\cftdotsep}}
\renewcommand{\cftsecleader}{\cftdotfill{\cftdotsep}}
\setlength{\cftsecindent}{2.2em}
\setlength{\cftsubsecindent}{4.2em}
\setlength{\cftsecnumwidth}{2em}
\setlength{\cftsubsecnumwidth}{2.5em}

\titlespacing\section{0pt}{12pt plus 4pt minus 2pt}{0pt plus 2pt minus 2pt}
\titlespacing\subsection{0pt}{12pt plus 4pt minus 2pt}{0pt plus 2pt minus 2pt}


\begin{document}
\titleformat{\section}
{\normalfont\fontsize{15}{0}\bfseries}{\thesection}{1em}{}
\titlespacing{\section}{0cm}{0.5cm}{0.15cm}
\titleformat{\subsection}
{\normalfont\fontsize{13}{0}\bfseries}{\thesubsection}{0.5em}{}
\titlespacing{\section}{0cm}{0.5cm}{0.15cm}

%=============================================================================

\pagenumbering{Alph}
\begin{titlepage}
\begin{flushright}
\includegraphics[width=4cm]{USyd}\\[2cm]
\end{flushright}
\center 
\textbf{\huge INFO1111: Computing 1A Professionalism}\\[0.75cm]
\textbf{\huge 2023 Semester 1}\\[2cm]
\textbf{\huge Self-Learning Report}\\[3cm]

\textbf{\huge Submission number: 2}\\[0.75cm]
\textbf{Github link:https://github.com/Junsen-Zhang-Chris/self-learning/blob/main/README.md
 }\\[2cm]

{\large
\begin{tabular}{|p{0.35\textwidth}|p{0.55\textwidth}|}
	\hline
	{\bf Student name} & Junsen Zhang\\
	{\bf Student ID} & 520163256\\
	{\bf Topic} & MySQL\\
	{\bf Levels already achieved} & A\\
	{\bf Levels in this report} & B\\
	\hline
\end{tabular}
}
\thispagestyle{empty}
\end{titlepage}
\pagenumbering{arabic}



%=============================================================================

\tableofcontents

%=============================================================================





\newpage
\section{Level A : Initial Understanding}
\vspace{5mm}
\subsection{Level A Demonstration}
      My goals:\\
--\qquad1.Have a good command of date types and variables.\\
--\qquad2.Create a database containing multiple tables.\\
--\qquad3.Learn key queries:select,insert,delete,update,where,order.\\


\subsection{Learning Approach}
At the very beginning, I searched all the information and materials about MySQL on the Internet, so as to facilitate my understanding and lay a foundation for my future study and mastery. Then I find the teaching content from multiple sources, including text, video and so on. After I downloaded the latest version of  MySQL and DBeaver from the official website,  I systematically learned from zero basis according to the teaching content system. Every time I learned something new, I would write it down and spend time doing it many times, so that I could learn more about the new content. Because of the variety of code commands that need to be mastered, I also review the previous content every day to prevent forgetting.



\subsection{Challenges and Difficulties}
I think the biggest challenge is remembering a large number of code commands, as many of them are similar and easily confused. What’s more, MySQL contains DDL, DML, DQL and DCL, and their functions are completely different, so the content to learn is also relatively large. But overall, it wasn't that different from the other tools I was learning, so most of my time was spent learning new code commands and mastering the basics. However, i also spent a lot of time mastering DBeaver, as it's a database connection software that makes it easy to write SQL scripting language on a daily basis, so mastering its usage is essential for anyone learning MySQL.

\subsection{Learning Sources}
Learning Source - What source did you use? (Note: Include source details such as links to websites, videos etc.). Contribution to Learning - How did the source contribute to your learning (i.e. what did you use the source for)?


\begin{tabular}{|p{0.45\textwidth}|p{0.45\textwidth}|}
	\hline
	Learning Source - What source did you use? (Note: Include source details such as links to websites, videos etc.). & Contribution to Learning - How did the source contribute to your learning (i.e. what did you use the source for)?\\
	\hline
 Website(https://www.w3schools.com/) & I get tutorials and work on the website.\\
	\hline
	Videos( https://b23.tv/JgA33oi) & I watch a lot of  instructional videos of MySQL on this app(website)\\
	\hline
	Videos(https://b23.tv/dBweThq) & I watch a lot of  instructional videos of MySQL on this app(website)\\
	\hline
	Information(https://www.talend.com/) & I get enough information of MySQL from it.\\
	\hline
	Videos(https://b23.tv/N5LM4IQ) & I learn the usage of DBeaver from it.\\
	\hline
\end{tabular}

\subsection{Application artifacts}




\begin{figure}[h]
\headrule % 图像居中
\includegraphics[width=0.6\textwidth]{1.png} % 插入图像
\end{figure}

This is the basic operation of MySQL on the terminal:


Create database  + name + ; ==  Create a randomly named database.

Show database;  ==   Search all databases on your desktop and display them.

Select database();   ==  Search the database which you are using right now and display it.

Use + database’s name + ;   ==   Select out the database which you want to use.

Drop database + name + ;    ==   Delete the database.











\begin{figure}[h]
\headrule % 图像居中
\includegraphics[width=0.6\textwidth]{2.png} % 插入图像
\end{figure}

 
Create table + name + (.....)  +; == Create your table in the database.

Int == The numbers that need to be filled in the form are integers.

Varchar(x) ==  The number of words you fill in here is less than x.

Decs + table’s name + ; ==  Query the structure of your custom table.



























\begin{figure}[H]
\headrule % 图像居中
\includegraphics[width=0.6\textwidth]{3.png} % 插入图像
\end{figure}











 

Alter table + table’s name + (rename) + new name +  ; ==  Change the table’s name.

Eg.We can also change the command in () except ‘rename’ such as, ‘modify’, ‘change’, ‘drop’.

Drop table + table’s name + ;  ==  Delete the table.




 


\begin{figure}[h]
\headrule % 图像居中
\includegraphics[width=0.6\textwidth]{4.png} % 插入图像
\end{figure}

This is the operation in DBeaver:

Insert into +table’s name + values(.....) == Add information to the table.
What’s more.


Update + table’s name + set + xx=yy(where +condition) == change the table’s name from xx to yy in the condition of.....

We can also use “delete from” to replace the”update”  means delete xx from the table.


%=============================================================================

\newpage
\section{Level B: Basic Application}
Whilst level A is about doing something simple with the topic to just show that you have started to be able to use the tool or technology, level B is about doing something practical that might actually be useful.

\subsection{Level B Demonstration}

At level B, I try to develop a simple inventory management application. Since it is the first time to develop a application, not only do i watch the teaching videos, I also make appropriate reference to some established products and borrow some highlights from them.\\ The application can now be implemented simply and basically: Users interact with the MySQL database backend to add, update, view, and remove products from the store inventory. For better development, I also use Python and its MySQL connector library to create applications.


\subsection{Application artifacts}
Firstly, i design an appropriate database schema to store and manage product data on the terminal:

Create table products (
    \\id int auto\_ increment primary key, 
    \\name varchar(255) not null,
    \\description text,
    \\price decimal(10, 2) not null,
    \\quantity int not null
\\);


Secondly, to create my application, I choose Python as  programming language as it has a MySQL connector library that makes it easy to interact with a MySQL database. And then using the mysql-connector-python library to connect to my MySQL database and execute SQL queries:


Import  mysql.connector

db = mysql.connector.connect(
  \\host="local",
  \\user="Chris",
  \\password="junsenzhang",
  \\database="inventory"
)

cursor = db.cursor()

cursor.execute("SELECT * FROM products")

rows = cursor.fetchall()

db.close()


Then, i create the user interface, by using the Flask:


from flask import Flask, render\_template
import mysql.connector

app = Flask(\_\_name\_\_)

@app.route('/')
def index():
    
   \qquad db = mysql.connector.connect(
       \\host="local",
       \\user="Chris",
       \\password="junsenzhang",
       \\database="inventory"
)

    \qquad cursor = db.cursor()

    \qquad cursor.execute("SELECT * FROM products")

    \qquad rows = cursor.fetchall()

    \qquad db.close()

    \qquad return render\_template('index.html', products=rows)




What’s more, there are also some methods to handle user input and validate user input to prevent errors and security vulnerabilities:

1. adding a new product:

@app.route('/add', methods=['POST'])
\\def add():
    \\name = request.form['name']
    \\description = request.form['description']
    \\price = request.form['price']
    \\quantity = request.form['quantity']

    db = mysql.connector.connect(
      \\host="local",
      \\user="Chris",
      \\password="junsenzhang",
      \\database="inventory"
    )

    cursor = db.cursor()

    cursor.execute("INSERT INTO products (name, description, price, quantity) VALUES (\%s, \%s, \%s, \%s)", (name, description, price, quantity))

    db.commit()

    db.close()

    return redirect('/')



2. deleting a product:


@app.route('/delete/<int:id>', methods=['POST'])
def delete(id):
    \\try:
      







%=============================================================================









\newpage
\section{Level C: Deeper Understanding}
Level C focuses on showing that you have actually understood the tool or technology at a relatively advanced level. You will need to compare it to alternatives, identifying key strengths and weaknesses, and the areas where this tool is most effective.


\subsection{Strengths}
One of the key strengths of MySQL is its scalability.   It can handle large amounts of data and can efficiently manage high-traffic websites and applications.   MySQL also offers excellent performance, enabling fast data retrieval and processing.   It supports various operating systems and has extensive community support, providing a wealth of resources, documentation, and user forums.   Additionally, MySQL is open source, making it cost-effective and allowing for customization and integration with other tools and technologies.


\subsection{Weaknesses}
One of the key weaknesses of MySQL is its limited support for complex transactions. While it supports basic transactional features, it may not be suitable for applications that require advanced transaction management, such as multi-level transactions or distributed transactions. MySQL also lacks some advanced features found in other database systems, such as built-in support for full-text search or advanced analytical functions. In certain scenarios, MySQL's performance may degrade when dealing with extremely large datasets or complex queries.


\subsection{Usefulness}
One scenario where MySQL can be highly useful is in the management of a content management system (CMS) for a news website. MySQL can serve as the database backend to store and organize various types of data, including articles, authors, categories, and user information. With MySQL, you can efficiently store and retrieve large volumes of articles, perform complex queries to filter and sort content, and enable user authentication and authorization. The scalability and reliability of MySQL make it suitable for handling the continuous flow of news updates and user interactions in a high-traffic environment, ensuring smooth content management and delivery on the news website.


\subsection{Key Question 1}
What is a database key?\\

A database key is a unique identifier or attribute that is used to uniquely identify records within a database table. It ensures the integrity and uniqueness of data by providing a way to identify and access individual records. A key can be a single column or a combination of multiple columns in a table. The primary key is the main key that uniquely identifies each record, while a foreign key establishes a relationship between tables. Keys enable efficient searching, indexing, and retrieval of data, and they play a crucial role in maintaining the integrity and consistency of the database.


\subsection{Key Question 2}
Why might a user prefer to control a MySQL interface using a CLI rather than a GUI? \\

The reasons might be:

(1) A CLI provides more flexibility and control over the commands and operations performed on the database. Users can directly type commands, scripts, and queries, allowing for precise control and customization.

(2) A CLI is often faster and more efficient for experienced users who are comfortable with command-line operations. They can execute complex queries or perform repetitive tasks more quickly by using command shortcuts and scripting.

(3) A CLI is typically lighter in terms of system resources compared to a GUI, making it suitable for remote or low-bandwidth environments. It can be accessed via SSH or other remote protocols, enabling efficient management of databases on remote servers.
















%=============================================================================

\newpage

\bibliographystyle{ieeetran}
\bibliography{main}

\end{document}
\end{report}

