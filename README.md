# FormApplication

Running the Database File in SQL Server Management Studio (SSMS) for a .NET Project
This guide will help you set up and run a .db file in SQL Server Management Studio (SSMS) for use in your .NET project.

Prerequisites
Before you begin, ensure that you have the following installed:

1. SQL Server Management Studio (SSMS)
2. SQL Server: Ensure you have an instance of SQL Server running.
3. .NET SDK: Install the .NET SDK from the official .NET website.
   
Steps to Run the .db File

You can find the db file to the Under Database folder

1. Open SQL Server Management Studio (SSMS)
Open SSMS.
Connect to your SQL Server instance by selecting your server name and providing the necessary credentials.
2. Attach the .db File
In the Object Explorer, right-click on the Databases node and select Attach....
In the Attach Databases window, click on the Add... button.
Browse to the location of your .db file (typically a .mdf file for SQL Server) and select it.
Click OK to attach the database.
Note: Ensure that the .ldf (log file) is also in the same directory. If it is missing, SQL Server will attempt to rebuild it.

3. Verify the Database Connection
Once attached, expand the Databases node in the Object Explorer to verify that your database appears in the list.

4. Update Connection Strings in Your .NET Project
Open your .NET project in your IDE (e.g., Visual Studio).

Locate your connection string present in Utility folder.

Update the connection string to point to the attached database. Here’s an example connection string:

json
Copy code
"ConnectionStrings": {
  "DefaultConnection": "Server=YourServerName;Database=YourDatabaseName;User Id=YourUsername;Password=YourPassword;"
}
Replace YourServerName, YourDatabaseName, YourUsername, and YourPassword with your actual server and database credentials.

5. Running the Project
Once your database connection is configured, you can run your .NET project.
The application should now be able to interact with the SQL Server database.

Initially the login credentials after run the project is:

Email - abc@gmail.com
Password - 1234

Troubleshooting
Database Not Appearing: Ensure that the .db file is compatible with SQL Server and that you have the necessary permissions to attach the database.
Connection Issues: Double-check the connection string for typos or incorrect credentials. You may need to verify that the SQL Server instance is running.

Note: If any help required please write me at: akshaykishore8@gmail.com
