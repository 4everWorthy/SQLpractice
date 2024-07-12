# SQLpractice

C:\Users\admin>cd sqlite3
The system cannot find the path specified.

C:\Users\admin>cd sqlite

C:\Users\admin\sqlite>sqlite3 Bookstore.db
SQLite version 3.46.0 2024-05-23 13:25:27 (UTF-16 console I/O)
Enter ".help" for usage hints.
sqlite> CREATE TABLE Books (
(x1...> BookID INTERGER PRIMARY KEY,
(x1...> Title TEXT NOT NULL,
(x1...> Author TEXT NOT NULL,
(x1...> PublicationYear INTERGER,
(x1...> Price REAL);
Parse error: table Books already exists
  CREATE TABLE Books ( BookID INTERGER PRIMARY KEY, Title TEXT NOT NULL, Author
               ^--- error here
sqlite> Price REAL
   ...> );
Parse error: near "Price": syntax error
  Price REAL );
  ^--- error here
sqlite> DROP TABLE Books
   ...> DROP TABLE Books;
Parse error: near "DROP": syntax error
  DROP TABLE Books DROP TABLE Books;
                   ^--- error here
sqlite> DROP TABLE bOOKS;
sqlite> CREATE TABLE Books (
(x1...> BookID INTERGER PRIMARY KEY,
(x1...> Title TEXT NOT NULL,
(x1...> Author TEXT NOT NULL,
(x1...> PublicationYear INTERGER,
(x1...> Price REAL
(x1...> );
sqlite> INSERT INTO Books (Title, Author, PublicationYear, Price) VALUES ('One Piece', 'Eiichiro Oda', 1997, 7.99);
sqlite> INSERT INTO Books (Title, Author, PulbicationYear, Price) VALUES ('Naruto', 'Masashi Kishimoto', 1999, 9.99);
Parse error: table Books has no column named PulbicationYear
sqlite> INSERT INTO Books (Title, Author, PublicationYear, Price) VALUES ('Naruto', 'Masashi Kishimoto', 1999, 9.99);
sqlite> INSERT INTO Books (Title, Author, PublicationYear, Price) VALUES ('Attack on Titan', 'Hajime Isayama', 2009, 10.
99);
sqlite> INSERT INTO Books (Title, Author, PublicationYear, Price) VALUES ('My Hero Academia', 'Kohei Horikoshi', 2016, 8.99);
sqlite> INSERT INTO Books (Title, Author, PublicationYear, Price) VALUES ('Demon Slayer', 'Koyoharu Gotoug', 2016, 11.99);
sqlite> SELECT * FROM Books;
|One Piece|Eiichiro Oda|1997|7.99
|Naruto|Masashi Kishimoto|1999|9.99
|Attack on Titan|Hajime Isayama|2009|10.99
|My Hero Academia|Kohei Horikoshi|2016|8.99
|Demon Slayer|Koyoharu Gotoug|2016|11.99
sqlite> SELECT * FROM Books WHERE PublicationYear > 2000;
|Attack on Titan|Hajime Isayama|2009|10.99
|My Hero Academia|Kohei Horikoshi|2016|8.99
|Demon Slayer|Koyoharu Gotoug|2016|11.99
sqlite> SELECT * FROM Books WHERE Author = 'Hajime Isayama';
|Attack on Titan|Hajime Isayama|2009|10.99
sqlite> UPDATE Books
   ...> SET Price = 12.99
   ...> WHERE Title = 'Naruto';
sqlite> SELECT * FROM Books WHERE Title = 'Naruto;
'  ...> SELECT * FROM Books WHERE Title = 'Naruto;
Parse error: near "Naruto": syntax error
  tle = 'Naruto; SELECT * FROM Books WHERE Title = 'Naruto;
                                      error here ---^
sqlite> SELECT * FROM Books WHERE Title = 'Naruto';
|Naruto|Masashi Kishimoto|1999|12.99
sqlite> DELETE FROM Books
   ...> WHERE Title = 'Demon Slayer';
sqlite> SELECT * FROM Books WHERE Title = 'Demon Slayer';
sqlite> SELECT * FROM Books
   ...> SELECT * FROM Books WHERE Title = 'Demon Slayer';
Parse error: near "SELECT": syntax error
  SELECT * FROM Books SELECT * FROM Books WHERE Title = 'Demon Slayer';
                      ^--- error here
sqlite> SELECT * FROM Books;
|One Piece|Eiichiro Oda|1997|7.99
|Naruto|Masashi Kishimoto|1999|12.99
|Attack on Titan|Hajime Isayama|2009|10.99
|My Hero Academia|Kohei Horikoshi|2016|8.99
sqlite>

Reflection
After working with SQL today, I’ve learned that its structured and declarative nature makes it much easier to understand and use compared to JavaScript. Simple commands such as SELECT, INSERT, UPDATE, and DELETE align well with human thinking and problem-solving patterns, making it easier to manipulate and retrieve data. Additionally, the focus on relational data models mirrors how we naturally categorize and relate information. We also see this data model in many everyday applications, from online shopping to social media, where data is organized into tables to manage users and products.

