**#Employee Database Management App (Oracle + Java JDBC)**


**#Project Description**

This is a **Java Console Application** built using **JDBC (Java Database Connectivity)** to interact with an **Oracle Database**. It performs basic **CRUD operations** (Create, Read, Update, Delete) on an `employee` table.

The project is ideal for learning how to:
- Connect Java applications to Oracle DB.
- Use `Connection`, `PreparedStatement`, and `ResultSet` classes.
- Perform secure and efficient SQL operations from Java.

#Tools & Technologies

- Java (JDK 8 or above)
- Oracle Database (XE or Standard Edition)
- JDBC Driver for Oracle (`ojdbc8.jar`)
- IDE: IntelliJ IDEA / Eclipse / VS Code
- SQL Developer (optional)

**#Project Structure**       
com.jdbc      
├── EmployeeDatabaseApp.java # Main menu and user interaction logic       
├── DBManager.java # Handles all JDBC database operations

**#Database Table Structure (Oracle SQL)**

Before running the application, execute the following SQL to create the `employee` table:

CREATE TABLE employee (          
    id NUMBER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,           
    name VARCHAR2(100),      
    age NUMBER         
);


**#JDBC Connection Settings**

In the DBManager class:        
Class.forName("oracle.jdbc.driver.OracleDriver");         
con = DriverManager.getConnection(         
    "jdbc:oracle:thin:@localhost:1522:ORCL",  // Update if your SID/port is different          
    "YourDB-Name",                             // Your DB username            
    "YourPassword"                                   // Your DB password            
);

**#Ensure:**    
-Oracle DB is running.        
-Correct SID, username, and password are provided.           
-ojdbc8.jar is in your classpath.       

**#Features:**
-Add new employee (name, age)        
-View all employees           
-Update employee by ID            
-Delete employee by ID           
-Graceful exit and connection closing           

**#Sample Menu (Console)**        
===== Employee Database App =====           
1. Add Employee         
2. View All Employees        
3. Update Employee           
4. Delete Employee          
5. Exit        
Enter your choice:            

**#How to Run**
**1.Compile & Run the Java File:**      
javac -cp .;ojdbc8.jar com/jdbc/EmployeeDatabaseApp.java     
java -cp .;ojdbc8.jar com.jdbc.EmployeeDatabaseApp       

**2.Inside IDE (Eclipse/IntelliJ):**            
Add ojdbc8.jar to your project libraries.      
Run EmployeeDatabaseApp class.         

**#Key Concepts Covered**        
-Java JDBC API (Connection, PreparedStatement, ResultSet)       
-Oracle SQL integration           
-Secure SQL operations with prepared statements             
-Exception handling & resource management (try-with-resources)               
-Modular design (DBManager pattern)          

**#Learning Outcome**           
By building this project, you will learn:       

-How to set up JDBC with Oracle DB.           
-How to perform SQL queries and updates safely from Java.          
-How to structure small database-driven Java apps.          






