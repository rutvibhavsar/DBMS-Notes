# DBMS-Notes
## Introduction (:star: = IMP)
### What is Data?
- **Data** is a collection of a distinct small unit of information. It can be used in a variety of forms like text, numbers, media, bytes, etc. and it can be stored in pieces of paper or electronic memory, etc.
### What is Database?
- A __database__ is an organized collection of data, so that it can be easily accessed and managed. 
- The main purpose of the database is to operate a large amount of information by storing, retrieving, and managing data.
- There are many databases available like *MySQL, Sybase, Oracle, MongoDB, Informix, PostgreSQL, SQL Server*, etc.
### What is DBMS?
- A *database management system* is a system designed to allow you to query the data that is in the database and make modifications to the database.
- *Database management system* is the software that is used to access and manage one or more databases that contain the actual data.
### Why do we need DBMS?
- DBMS can be used for:
  - Creation of Database
  - Retrival of information from the database
  - Updating the database
  - Managing the database
- DBMS also provide following functionalities:
  1. Processing query and object management
  2. Controlling redundncy and inconsistency
  3. Efficient memory management and indexing
  4. Concurrency control and transaction management
  5. Access control and ease in accessing data
  6. Integrity constraints
  7. Multiple User Interface
  8. Data Scalability, Expandability and Flexibility
  9. Security
- [Read more..](https://www.geeksforgeeks.org/need-for-dbms/ "GFG Link")
### ACID Property :star:
- **Atomicity**: It can manage a set of operations as a single "unit", so either everything succeeds or everything is aborted and comes back to the previous state.
- **Consistency**: Basically, things are only saved if they respect all kinds of requirements defined by the database administrator.
- **Integrity**: You can have 10 people working on the same database simultaneously and the resulting state is exactly the one you expect if those 10 people worked on the database one by one.
- **Durability**: Things are actually saved in a non-volatile memory (so not just in RAM).
### DBMS v/s File System
- | DBMS | File System |
  | ---- | ----------- |
  |Multi-user access | Does not support multi-user access|
  |Designed to fulfill need of small and large business|Only limited to smaller Database|
  |Remove redundancy and integrity|Redundancy and intergrity issues|
  |Expensive. But in long term, total cost of ownership is cheaper|It's Cheaper|
  |Easy to implement complicated transactions|No support for complcated transaction|
  |Provides good protection|Difficult to provide protection|
### Functions of DBA
- DBA stands for **Database Administrator**. Functions include:
  - **Schema Definiton**:  The DBA creates the original database schema by executing a set of data deﬁnition statements in the DDL.
  - **Storage structure and access-method deﬁnition.**
  - **Schema and physical-organization modiﬁcation**: The DBA carries out changes to the schema and physical organization to reﬂect the changing needs of the organization, or to alter the physical organization to improve performance.
  - **Granting of authorization for data access**: By granting different types of authorization, the database administrator can regulate which parts of the database various users can access. The authorization information is kept in a special system structure that the database system consults when ever someone attempts to access the data in the system.
  - **Routine Maintainance**:
    - *Periodically backing up the database*, either onto tapes or onto remote servers, to prevent loss of data in case of disasters such as ﬂooding.
    - *Ensuring that enough free disk space is available* for normal operations, and upgrading disk space as required.
    - *Monitoring jobs running on the database* and ensuring that performance is not degraded by very expensive tasks submitted by some users. 
### 2-tier and 3-tier architecture
<img src='https://i2.wp.com/3.bp.blogspot.com/-5IYf6nhD5L4/VwQar9OpuQI/AAAAAAAAEbg/xXlzllw0Gfwjeud20Gjv7rzWOrnU7JM1A/s1600/two%2Btier%2Band%2Bthree%2Btier%2Barchitecture%2Bdbms%2Btanmayonrun.PNG' width='500' height='200'></img>
  |2-tier|3-tier|
  |------|------|
  |Its Client-Server architecture|Its a web based application|
  |The application logic is either buried inside the user interface on the client or within the database on the server (or both).|The application logic or process resides in the middle-tier, it is separated from the data and the user interface.|
  |Consists of two layer: Client tier and database(data tier)|Consists of three layer: Client, Business and Data|
  |Easy to build and maintain|Complex to build and maintain|
  |Runs slower|Runs faster|
  | Less secured as client can communicate with database directly.| Secured as client is not allowed to communicate with database directly.|
  |Performance loss when users increases|Gives more performance|
  |Example: When you go to bank to open an account./When you go to the station to book tickets|Example: When you use the website to book your tickets|
  
### Database Languages (DDL, DQL, DML, DCL and TCL)
- **SQL(Structured Query Language)**  is the database language by the use of which we can perform certain operations on the existing database and also we can use this language to create a database. SQL uses certain commands like Create, Drop, Insert, etc. to carry out the required tasks.
- These SQL commands are mainly divided into following categories:

  1. **DDL(Data Definition Language)** : It  consists of the SQL commands that can be used to define the database schema. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
 
    -  **CREATE** :  is used to create the database or its objects (like table, index, function and views).
    -  **DROP** : is used to delete the objects from database.
    -  **ALTER** : is used to alter the structure of database.
    -  **TRUNCATE** : is used to remove all records from a table, including all spaces allocated for the records are removed.
    -  **COMMENT** : is used to add comments to the data directory.
    -  **RENAME** : is used to rename an object existing in the database.

  2. **DQL(Data Query Language)** used for performing queries on the data within schema objects. The purpose of the DQL Command is to get some schema relation based on the query passed to it.
    - **SELECT** : is used to retrive data from database.

  3. **DML(Data Manipulation Language)** : Commands used to manipulate the data present in databases belongs to DML and this includes most of the SQL statements.
    - **INSERT** : is used to insert data into a table.
    - **UPDATE** : is used to update existing data within a table.
    - **DELETE** : is used to delete records from a database table.


  4. **DCL(Data Control Language)** : mainly deal with the rights, permissions and other controls of the database system. 
    - **GRANT** : gives users access privileges to the database.
    - **REVOKE** : withdraw user’s access privileges given by using the GRANT command.


  5. **TCL(Transaction Control Language)** : deals with transaction within database.
    - **COMMIT** : commits a transaction.
    - **ROLLBACK** : rollbacks a transaction in case of any error occurs.
    - **SAVEPOINT** : sets a savepoint in transaction.
    - **SET TRANSACTION** : specifiy characteristics of the transaction.
### Instance, Schema and Sub-Schema:
- Information/data in database at particular moment is known as ***instance***, physical arrangement of data as it appears in database can be defined as ***schema***, and the logical view of data as it appears to the application can be called as ***sub-schema***.
### Data Models
- Read [here](https://afteracademy.com/blog/what-is-data-model-in-dbms-and-what-are-its-types)
### Data Abstraction
- Data Abstraction refers to the process of hiding irrelevant details from the user.
- **Example**: If we want to access any mail from our Gmail then we don't know where that data is physically stored i.e is the data present in India or USA or what data model has been used to store that data? We are not concerned about these things. We are only concerned with our email. So, information like these i.e. location of data and data models are irrelevant to us and in data abstraction, we do this only. 
- We hide the unnecessary data from the user and this process of hiding unwanted data is called Data Abstraction.

### 3 Levels of Data Abstraction
- There are mainly *three* levels of data abstraction and we divide it into three levels in order to achieve **Data Independence**. **Data Independence** means users and data should not directly interact with each other. The user should be at a different level and the data should be present at some other level. By doing so, Data Independence can be achieved.
1. **View Level or Externam Schema**
- This level tells the application about how the data should be shown to the user.
- *Example*: As a student, we can view our marks, attendance, fee structure, etc. But the faculty of the university will have a different view. He will have options like salary, edit marks of a student, enter attendance of the students, etc. So, both the student and the faculty have a different view. 
- So, different users will have a different view according to the authorization they have.
2. **Conceptual level or Logical level**
- This level tells how the data is actually stored and structured. We have different data models by which we can store the data.
- Though the data is stored in the database but the structure of the tables like the student table, teacher table, books table, etc are defined here in the conceptual level or logical level. Also, how the tables are related to each other are defined here. Overall, we can say that we are creating a blueprint of the data at the conceptual level.
3. **Physical level or Internal schema**
- Physical level tells us that where the data is actually stored i.e. it tells the actual location of the data that is being stored by the user.
- The Database Administrators(DBA) decide that which data should be kept at which particular disk drive, how the data has to be fragmented, where it has to be stored etc. They decide if the data has to be centralized or distributed. Though we see the data in the form of tables at view level the data here is actually stored in the form of files only.
