# Test Cases
We have yet to create any solid full fledged test cases as we are still in the process of getting implemented code
up and running correctly before we reach the testing phase. 

## Unit tests
The simples use of the cybercommons API is to simply add two numbers through distrubited message passing and make sure they are
outputted through the framework correctly.
For unit tests we will be implementing simple tests that check for basic functionality of our code when completed such as addition checking. This is the simplest case that can be ran to ensure correct communication with the API

### Unit test outline:
1. Ensure username and password of admin is correct. Ensure only they have access to the database.
2. Click on ogin button takes admin to the database application through Rest API
3. Add and manipulate JSON file within the application, and ensure changes take place
4. Add field to a document and it can be stored within MongoDB 
5. Unit test must ensure the previous tasks are executed correctly through the provided message passing system within the cybercommons framework

## System tests
For system tests we simply run the api with the help of docker given that we all run on different operating systems as well as other possible users of the api. To ensure the system runs correctly we are able to check docker to make sure all versions:
cybercommons_cybercom_mongo_1  

cybercommons_cybercom_memcache_1 

cybercommons_cybercom_rabbitmq_1 

cybercommons_cybercom_api_1   

cybercommons_cybercom_celery_1

If theses are all running smooth when we run [docker-compose up -d] we know the Django Rest Framework API has been setup correctly

### System test outline:
1. Does the application launch properly with Docker and Docker Compose? Yes, Docker is a container independent of the OS. It can be deployed quickly.
2. Can a user register to use the framework and database? Yes we tested for user registration using the web application.
3. Does the application launch properly for all different OS and web browsers? Yes as it uses Docker whihc allows this.
4. Functionalities such as searching, sorting, filtering, adding? We have tested the application by adding our own JSON documents into the framework. This application can search and filter keywords within the document to a certain extent. However we have noticed a few small bugs that still need to be sorted out with these functionalities

## Acceptance tests
For acceptance tests we ensure that the configured API correctly runs http://localhost:8080 on the users local computer. If this runs correctly with the login and password that cybercommons provides, we know that the user has been acceptance into the database. Originally we had some troubles with the port numbers incorrectly being set in which case we were not able to access the url site. After some small modifications this has been corrected when running small acceptance tests.

### Acceptance test outline:
