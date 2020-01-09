Description 
========================================
This project is designed to take input body from user along with the Username and Password. Once the Credentials are matched from the properties file, It will display the desired response else will log as "Authentication Failed".

Gives a basic insight on how to set headers/body and NOT use hard-coded stuff in code.

Request :- 
==> curl -XPOST -H 'Username:ESB_User1' -H 'Password:redhat' --data '{"Print Details"}' http://localhost:9001/esb/project2

Response :- {"Name": "ESB_User1" , "Age":"25" , "ResponseMessage":"Hello World!!"}

If you pass wrong credentials in Headers, It will give Response as Authentication failed.
Request :- 
==> curl -XPOST -H 'Username:ESB_User2' -H 'Password:redhat123' http://localhost:9001/esb/project2

Response :- {"ResponseMessage":"Authentication Failed"}

### Additional Comments are added in the blueprint ###

========================================
To build this project use

    mvn install

To run the project you can execute the following Maven goal

    mvn camel:run
