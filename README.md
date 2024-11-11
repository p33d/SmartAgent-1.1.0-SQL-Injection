# SmartAgent-1.1.0-SQL-Injection
SmartAgent version 1.1.0 suffers from multiple unauthenticated remote SQL injection vulnerabilities


This script allows an unauthenticated user to exploit SQL Injection vulnerabilities in the SmartAgent v1.1.0 web application. The script provides three different options for exploiting known vulnerable endpoints.
Prerequisites

    Python 3.x installed
    requests library installed (pip install requests)
    An authorized environment for testing purposes (please note: unauthorized access or testing is illegal).

How to Use the Script
Step-by-Step Instructions

    Install Dependencies
    Before running the script, make sure to install the required dependencies using:

pip install requests

Run the Script
Execute the script using the command:

python smartagent_exploit.py

(Replace smartagent_exploit.py with the actual filename you saved the script as).

Choose the Endpoint to Exploit
After running the script, you will be prompted to choose one of three available endpoints:

Choose the endpoint to exploit:
1. POST request to interface.php (action=exportNetworkDate)
2. GET request to sendPushManually.php (id parameter)
3. GET request to recuperaLog.php (client parameter)
Enter the number of the endpoint you want to exploit:

    Option 1: Exploits the interface.php endpoint using a POST request.
    Option 2: Exploits the sendPushManually.php endpoint using a GET request.
    Option 3: Exploits the recuperaLog.php endpoint using a GET request.

Enter the Target URL
You will be asked to provide the target URL. Enter the full URL of the server you want to test. For example:

Enter the target URL (e.g., https://smartagent.example.com):

Enter the SQL Command
After specifying the target URL, you will be prompted to enter the SQL command to run. For example:

    Enter the SQL command you want to run (EX: UNION SELECT @@version):

    This is where you can insert an SQL query to test the vulnerability.

    View the Response
    After submitting the SQL command, the script will send the request to the target URL and print the response from the server. This will allow you to observe any potential database responses or errors.

Example Usage

    Run the script:

python smartagent_exploit.py

Select the endpoint:

Enter the number of the endpoint you want to exploit: 1

Provide the target URL:

Enter the target URL (e.g., https://smartagent.example.com):

Enter the SQL command to inject:

    Enter the SQL command you want to run (EX: UNION SELECT @@version):

    The server's response will be printed, displaying any successful SQL query output or error.

Important Note

Disclaimer: This script is for educational purposes only. Unauthorized access or testing against systems without explicit permission is illegal and unethical. Use this script responsibly.
License

This project is licensed under the MIT License. See the LICENSE file for more details.
