# Troubleshooting MySQL/MariaDB Port 3306 Conflict

If you're encountering issues with port 3306 being in use, preventing MySQL/MariaDB from starting, follow these steps to resolve the conflict.

## Step 1: Identify Processes Using Port 3306

Open a command prompt and run the following command to identify processes using port 3306:

```bash
netstat -ano | find "3306"
