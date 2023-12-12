# Troubleshooting MySQL/MariaDB Port 3306 Conflict

If you're encountering issues with port 3306 being in use, preventing MySQL/MariaDB from starting, follow these steps to resolve the conflict.

## Step 1: Identify Processes Using Port 3306

Open a command prompt and run the following command to identify processes using port 3306:

```bash
netstat -ano | find "3306"
## Step 2: Stop Conflicting Process

2.1. Open Task Manager by pressing `Ctrl + Shift + Esc`.

2.2. Go to the "Details" tab.

2.3. Find the process with the matching PID from Step 1.

2.4. Right-click on the process and select "End Task" or "End Process."
