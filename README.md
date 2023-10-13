# customerrewards

This application is for calculating the rewards of the customers based on the amount spent.

Local Setup for running this application :
1. Need an IDE like STS or IntelliJ
2. MySQL Workbench and MySQL command line client
3. Postman
4. Git bash

Steps for starting the application :
1. Start the MySQL server by configuring the Environmental variables.
2. Copy the bin location path of MySQL server into the path section of system environmental variables.
3. Start the MySQL command line client and provide the password.
4. Password is in the application property file.
5. Once the server starts create a schema with name "reward".
6. Import the code into any IDE and start the RewardsApplication.
7. The application starts on port 9090.

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