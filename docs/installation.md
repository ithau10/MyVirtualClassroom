# Installation Guide

Follow these steps to set up and run MyVirtualClassroom locally.

## Prerequisites

1. **Visual Studio:** [Download and install Visual Studio](https://visualstudio.microsoft.com/downloads/)
2. **.NET SDK:** [Download and install .NET SDK](https://dotnet.microsoft.com/download)
3. **SQL Server:** [Download and install SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-downloads)

## Clone the Repository

### Using Bash

```bash
git clone https://github.com/ithau10/MyVirtualClassroom.git
cd MyVirtualClassroom
```

### Without Bash

**Visit the repository:** [MyVirtualClassroom GitHub Repository](https://github.com/ithau10/MyVirtualClassroom)

## Set Up Database

1. **Open SQL Server Management Studio (SSMS).**

2. **Connect to your SQL Server instance using the following steps:**
   - Launch SQL Server Management Studio.
   - In the "Connect to Server" dialog, enter the necessary information for your SQL Server instance (Server Name, Authentication, etc.).
   - Click "Connect."

3. **Create the "Oteaching" database using the graphical interface:**
   - In the Object Explorer, expand the "Databases" node.
   - Right-click on the "Databases" node and choose "New Database..."
   - In the "New Database" dialog, enter "Oteaching" as the Database name.
   - Configure any additional settings as needed.
   - Click "OK" to create the database.



# Run the Program via Visual Studio

1. **Open Visual Studio Code:**
   - Launch Visual Studio Code on your machine.

2. **Open the MyVirtualClassroom :**
   - Click "File" > "Open Folder" and navigate to the location where you cloned the MyVirtualClassroom repository and click open.

3. **Set Default.aspx.cs as Start Page**

      i. **Open the Solution Explorer:**
         - In Visual Studio, locate and open the Solution Explorer. You can usually find it on the right side of the Visual Studio window.
      
      ii. **Locate the `Default.aspx` File:**
         - In the Solution Explorer, find the `Default.aspx` file under your project's web pages or views.
      
      iii. **Set as Start Page:**
         - Right-click on the `Default.aspx` file.
         - Choose "Set as Start Page" from the context menu.
      
      iv. **Save Changes:**
         - Click "Save" or "OK" to save your changes.

4. **Set up the Database Connection:**
   - Open the `web.config` file in your project.
   - Locate the `"ConnectionString"` under `"ConnectionStrings"`.

     
     ```xml
     <connectionStrings>
        <add name="OTeachingConnectionString" connectionString="Data Source=DESKTOP-1P0GCC5;Initial Catalog=OTeaching;Integrated Security=True" providerName="System.Data.SqlClient"/>
         <add name="OTeaching" connectionString="Data Source=DESKTOP-1P0GCC5;Initial Catalog=OTeaching;Integrated Security=True"/>
      <add name="OTeachingConnectionString2" connectionString="Data Source=DESKTOP-1P0GCC5;Initial Catalog=OTeaching;Integrated Security=True" providerName="System.Data.SqlClient"/>
 
     </connectionStrings>
     ```
      
     

   - Update the connection string with your SQL Server details.

   - Alternatively, you can use the Visual Studio Tools Tab:
     - In Visual Studio, open the "View" menu and select "Server Explorer" or "Database Explorer."
     - Right-click on "Data Connections" and choose "Add Connection."
     - In the "Add Connection" dialog, enter your SQL Server details.
     - Click "Test Connection" to ensure it's successful.
     - Click "OK" to close the dialog and save the connection.



5. **Build the Solution:**
   - In Visual Studio Code, open the "View" menu and select "Solution Explorer."
   - Right-click on the solution file in the Solution Explorer.
   - Choose "Build" to build the solution.

6. **Run the Application:**
   - Right-click on the project or solution in the Solution Explorer.
   - Choose "Set as StartUp Project" if not already set.
   - Press `F5` or click the "Start Debugging" button to run the application.

7. **Access MyVirtualClassroom:**
   - Once the application is running, open your web browser.
   - Navigate to `http://localhost:5000` to access MyVirtualClassroom.

