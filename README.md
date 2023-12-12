# Troubleshooting MySQL/MariaDB Port 3306 Conflict

If you're encountering issues with port 3306 being in use, preventing MySQL/MariaDB from starting, follow these steps to resolve the conflict.

## Step 1: Identify Processes Using Port 3306

Open a command prompt and run the following command to identify processes using port 3306:  

`netstat -ano | find "3306"`  

## Step 2: Stop Conflicting Process

2.1. Open Task Manager by pressing `Ctrl + Shift + Esc`.

2.2. Go to the "Details" tab.

2.3. Find the process with the matching PID from Step 1.

2.4. Right-click on the process and select "End Task" or "End Process."
## Step 3: Stop MySQL/MariaDB Service

3.1. Open XAMPP Control Panel.

3.2. Stop the MySQL service.

## Step 4: Restart XAMPP

4.1. Close XAMPP Control Panel.

4.2. Reopen XAMPP Control Panel.

4.3. Start the MySQL service again.

## Step 5: Check Port Availability

Run the following command to check if port 3306 is now available:  

`netstat -ano | find "3306"`  
- If no results are returned, the port is now available.  

## Step 6: Change MySQL/MariaDB Port (Optional)

If conflicts persist, consider changing the MySQL/MariaDB port.

6.1. Open the `my.ini` or `my.cnf` configuration file (located in `xampp/mysql/bin`).

6.2. Find the line `port = 3306` and change the port number to an available value (e.g., 3307).

6.3. Save the file and restart the MySQL service.

## Step 7: Review Logs

Check the MySQL/MariaDB error logs for additional information:

- Logs are typically located in the `xampp/mysql/data` directory.
- Look for files named `error.log` or `mysql_error.log`.

## Conclusion

These steps should help resolve port conflicts and allow MySQL/MariaDB to start without issues. If problems persist, refer to the error logs for more detailed information.
