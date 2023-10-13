# customerrewards

This application is for calculating the rewards of the customers based on the amount spent.

Local Setup for running this application :
1. Install JDK preferably Java 1.8 and set the JAVA_HOME path
2. Install an IDE like STS or IntelliJ
3. Install MySQL and set path variable in the system environment variables
4. Install Postman
5. Install Git

Steps for starting the application:
1. Start the MySQL server by configuring the Environmental variables.
2. Start the MySQL command line client and provide the password.
3. Once the MySQL server starts create a schema with name "reward".
4. Clone the code into local machine using git commands
5. Import the code into any IDE.
6. The application sever port is given 9090 this can be configured in application property file.
7. Update the MySQL username and password in the application property file as per your system.
8. Run the application.

Postman Curls in Order :

1. curl --location 'http://localhost:9090/rewards/registration' \
--header 'Content-Type: application/json' \
--data-raw '{
    "firstName":"Warner",
    "lastName" :"David",
    "userName":"David_W",
    "emailId":"David_W@gmail.com",
    "mobileNumber":"2100546202"
}'

2. curl --location 'http://localhost:9090/rewards/transaction' \
--header 'Content-Type: application/json' \
--data '{
    "customerId":"52",
    "transactionAmount":"300"
}'

3. curl --location 'http://localhost:9090/rewards/reward_points/52'

4. curl --location 'http://localhost:9090/rewards/total_reward_points/52' \
--header 'startDate;' \
--header 'endDate;'
