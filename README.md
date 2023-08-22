# Little_Lemon_Analysis_and_Sales_Report

**Name: Yashwanth Reddy Surapareddy**
**University: Umass Lowell**

**Database Clients Project**

The following Software and Packages are installed for completing this project : 

1. Python

2. MySQL server

3. Jupyter notebook

4. MySQL Connector/Python API


**About the Project:**

Little-lemon is a restaurent and they want to create database and connect it with python to know their sales and analysis report
For that, this project used notebook to connect database with mysql.

The given steps are used to set up the Little Lemon database: 

**Step 1: Establish a connection:**

Use python API and import mysql.conector to import the required API package

**Step 2: Create a cursor:**

Once the connection between Python and MySQL database is successfully established, you need a cursor object to communicate with MySQL. 

**Step 3: Create the database and set it for use:**

Now that you have a connection and a cursor, create a new database little_lemon_db, and set the database for use.

**Step 4: Create tables and Insert data:**

Create and populate the tables in the little_lemon_db database: MenuItems table, Menu table, Bookings table, Orders table, and Employees table.

**Step 5: Implement and query stored procedures:**

Create a pool of connections, then draw a connection from it to carry out the following actions using stored procedures:

1. Create a pool with two connections and import MySQLConnectionPool to establish a connection.

2. Create and use the PeakHours stored procedure, which determines the peak or busiest hour for the restaurant based on the quantity of reservations.

3. Create and use the GuestStatus stored procedure, which returns the status of each guest's order based on the employee who is in charge of it.


**For routine MySQL database operations, stored procedures are developed. Every time you call a stored procedure, they ensure that the written SQL queries are executed in the same way since they are consistent. You just create a single stored procedure, which you then store in the MySQL database. In a Python-based application, the stored procedures can be called as often as necessary.**

The tasks and the steps that you must follow to complete each one are as follows:

**Task 1: Establish a connection**

Step one: Import MySQLConnectionPool

Step two: Import Error

Step three: Create a pool named pool_a with two connections. Use a try-except block to handle any possible errors. 

Step four: Obtain a connection from pool_a and create a cursor object to communicate with the database.


**Task 2: Implement a stored procedure called PeakHours**

Step one: Write a SQL CREATE PROCEDURE query for PeakHours

Use HOUR to extract the hour part from the BookingSlot.

Use COUNT to count the number of bookings.

Use GROUP BY on booking hour.

Use ORDER BY on the number of bookings in descending order.

Step two: Run the stored procedure query by invoking execute module on the cursor.

Step three: Invoke callproc to call the stored procedure.

Step four: Fetch the results in a variable called dataset.

Step five: Extract the names of the columns.

Step six: Print the names of the columns.

Step seven: Print the sorted data using for loop.


**Task 3: Implement a stored procedure GuestStatus**

Step one: Write a SQL CREATE PROCEDURE query for GuestStatus.

Step two: Combine the guest’s first and last name from the booking column using CONCAT. 

Step three: Use CASE to implement the following statuses for each guest’s order:

If the Role in the Employee table is Manager or Assistant Manager then the guest’s order status is Ready to pay

If the Role in the Employee table is Head Chef then the status is Ready to serve

If the Role in the Employee table is Assistant Chef then the status is Preparing Order

If the Role in the Employee table is Head Waiter then the status is Order served

Step four: LEFT JOIN Bookings table with Employees ON EmployeeID

Step five: Run the stored procedure query by invoking execute module on the cursor.

Step six: Invoke callproc to call the stored procedure.

Step seven: Fetch the results in a variable called dataset.

Step eight: Extract the names of the columns.

Step nine: Print the names of the columns.


**Task 4:**

Complete the following steps to establish a connection pool:

1. To create a connection pool, import MySQLConnectionPool class from MySQL Connector/Python.

2. To find the information on the error, import the Error class from MySQL Connector/Python.

3. Define your database configurations as a Python dictionary object called dbconfig.

4. Establish a connection pool [pool_name = pool_b] with two connections. 

5. Implement error handling using a try-except block in case the connection fails. 


**Task 5:**

Three guests are trying to book dinner slots simultaneously. Get the connections from pool_b and insert the following data in the Bookings table:

TIP: You need to add a connection to connect the third guest.

Guest 1:

1. Table Number: 8

2. First Name: Anees

3. Last Name: Java

4. Booking Time: 18:00

5. EmployeeID: 6

Guest 2:

1. Table Number: 5

2. First Name: Bald

3. Last Name: Vin

4. Booking Time: 19:00

5. EmployeeID: 6

Guest 3:

1. Table Number: 12

2. First Name: Jay

3. Last Name: Kon

4. Booking Time: 19:30 

5. EmployeeID: 6

Now, Return all the connections back to the pool. 

TIP: The pool size is two. However, you have three connected users. You can only return two connections. Returning a third connection will raise a PoolError. Use try-except to print the error message.  


**Task 6:**

Create a report containing the following information:

1. The name and EmployeeID of the Little Lemon manager.

2. The name and role of the employee who receives the highest salary.

3. The number of guests booked between 18:00 and 20:00.

4. The full name and BookingID of all guests waiting to be seated with the receptionist in sorted order with respect to their BookingSlot.


**Task 7:**

Create a stored procedure named BasicSalesReport that returns the following statistics: 

1. Total sales

2. Average sale

3. Minimum bill paid

4. Maximum bill paid


**Task 8:**

Little Lemon needs to display the next three upcoming bookings from the Bookings table on the kitchen screen to notify their chefs which orders are due next. To complete this task, carry out the following steps:

1. Get a connection from the pool.

2. Create a buffered cursor.

3. Combine the data from the Bookings and the Employee tables. Sort the retrieved records in ascending order. Then display the information of the first three guests. 

4. Returned the connection back to the pool.

5. The output should be as follows:

[BookingSlot]

[Guest_name]

[Assigned to: Employee Name [Employee Role]]

6. Print the sorted data using for loop.

7. Close the connection to return it back to the pool.




