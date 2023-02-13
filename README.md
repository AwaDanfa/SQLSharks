# SQLSharks
JustIT Training Assessment
Database Project Week
Introduction
You have been asked to develop a database for a local leisure centre, as they are in the process of upgrading their existing paper base record keeping system building for their swimming pool. They would like to use the database to help them manage their swimming lessons. Below are the entities and their attributes which were extracted from their paper-based system by a database developer who never got to implement the database for the local leisure centre. Use the entities and their attributes provided to create the respective tables. In addition, the leisure centre has now decided that they want one database. A database implemented using SQL database, preferably using MySQL workbench.   It is the view that once the databases are successfully implemented, the leisure centre would then decide which of the databases they would possibly integrate with a front-end Python application.  

•	Course (courseID, Level, Sessions, Instructor, startDate, LessonTime)
•	Lessons (LessonID, CourseID, MemberID) 
•	Members (MemberID, Firstname, Surname, DOB, Address, City)

The above highlighted in green are the primary keys.

EXERCISES:
A.	Use the SQL AND, OR and NOT Operators in your query (The WHERE clause can be combined with AND, OR, and NOT operators)
1.	Where courseID is equals to a number below 5 and the first name of any of the instructors 
2.	Where courseID is equals to a number above 5 and the lesson time is in the morning or afternoon. 

B.	Order by the above results by:
1.	 startDate in “course” table
2.	 MemberID in “members” table

C.	UPDATE the following:
1.	 Members table, change the addresses of any three members.
2.	Course table, change the startDate and lesson time for three of the sessions.

D.	Use the SQL MIN () and MAX () Functions to return the smallest and largest value 
1.	Of the LessonID column in the “lesson” table
2.	Of the membersID column in the “members” table 

E.	Use the SQL COUNT (), AVG () and SUM () Functions for these:
1.	Count the total number of members in the “members” table

2.	Count the total number of sessions in the” members” table
3.	Find the average session time for all “sessions” in course table 

F.	WILDCARD queries (like operator) 

a)	Find all the people from the “members” table whose last name starts with A.
b)	Find all the people from the “members” table whose last name ends with A.
c)	Find all the people from the “members” table that have "ab" in any position in the last name.
d)	Find all the people from the “members” table that that have "b" in the second position in their first name.
e)	Find all the people from the “members” table whose last name starts with "a" and are at least 3 characters in length:
f)	Find all the people from the “members” table whose last name starts with "a" and ends with "y"
g)	Find all the people from the “members” table whose last name does not starts with "a" and ends with "y"

G.	What do you understand by LEFT and RIGHT join? Explain with an example.
Use mockeroo to generate 20-50 record for each tables
Database format SQL



EXERCISES:
A.	Use the SQL AND, OR and NOT Operators in your query (The WHERE clause can be combined with AND, OR, and NOT operators)
1.	Where courseID is equals to a number below 5 and the first name of any of the instructors 
SELECT * FROM course;
SELECT * FROM course WHERE Instructor = 'Saliou';

2.	Where courseID is equals to a number above 5 and the lesson time is in the morning or afternoon. 
SELECT * FROM course WHERE courseID > 5 AND LessonTime = 'morning';


B.	Order by the above results by:

1.	 startDate in “course” table
SELECT * FROM Course ORDER BY startDate DESC; 

2.	 MemberID in “members” table
SELECT * FROM Members ORDER BY MemberID DESC; 

C.	UPDATE the following:
1.	 Members table, change the addresses of any three members.

UPDATE Members SET Address = 'X' WHERE MemberID = 1;
UPDATE Members SET Address = 'Y' WHERE MemberID = 2;
UPDATE Members SET Address = 'Z' WHERE MemberID = 3;

2.	Course table, change the startDate and lesson time for three of the sessions.
UPDATE Course SET startDate = "" AND lessonTime = "" WHERE ; 
UPDATE Course SET startDate = "" AND lessonTime = "" WHERE ; 
UPDATE Course SET startDate = "" AND lessonTime = "" WHERE ; 

D.	Use the SQL MIN () and MAX () Functions to return the smallest and largest value 
1.	Of the LessonID column in the “lesson” table
SELECT MIN(LessonID) FROM lessons;
SELECT MAX(LessonID) FROM lessons;

2.	Of the membersID column in the “members” table 
SELECT MIN(MemberID) FROM members;
SELECT MAX(MemberID) FROM members;

E.	Use the SQL COUNT (), AVG () and SUM () Functions for these:
1.	Count the total number of members in the “members” table
SELECT COUNT Members FROM members;

2.	Count the total number of sessions in the” members” table
SELECT COUNT (sessions) FROM members;

3.	Find the average session time for all “sessions” in course table 
SELECT AVG(sessions) FROM course;

F.	WILDCARD queries (like operator) 
a)	Find all the people from the “members” table whose last name starts with A.
SELECT * FROM members WHERE Lastname LIKE 'a%';

b)	Find all the people from the “members” table whose last name ends with A.
SELECT * FROM members WHERE Lastname LIKE '%a';

c)	Find all the people from the “members” table that have "ab" in any position in the last name.
SELECT * FROM members WHERE Lastname LIKE '%ab%';

d)	Find all the people from the “members” table that that have "b" in the second position in their first name.
SELECT * FROM members WHERE Firsttname LIKE '_b%';

e)	Find all the people from the “members” table whose last name starts with "a" and are at least 3 characters in length:
SELECT * FROM members WHERE Lastname LIKE 'a__%;

f)	Find all the people from the “members” table whose last name starts with "a" and ends with "y"
SELECT * FROM members WHERE Lastname LIKE 'a%y';

g)	Find all the people from the “members” table whose last name does not starts with "a" and ends with "y"
SELECT * FROM members WHERE Lastname NOT LIKE 'a%' AND NOT LIKE '%Y';

G.	What do you understand by LEFT and RIGHT join? Explain with an example.
The LEFT JOIN keyword returns all records from the left table (table1), and the matching records from the right table (table2). 
The result is 0 records from the right side, if there is no match.
SELECT * FROM members m
LEFT JOIN lessons l ON l.MemberID =  m.MemberID;
 
The RIGHT JOIN keyword returns all records from the right table (table2), and the matching records from the left table (table1). 
The result is 0 records from the left side, if there is no match.
SELECT * FROM course RIGHT JOIN lessons ON course.CourseID = lessons.MemberID;

Database format SQL
