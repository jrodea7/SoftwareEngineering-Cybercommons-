# Test Cases
We have yet to create any solid full fledged test cases as we are still in the process of getting implemented code
up and running correctly before we reach the testing phase. 

## unit tests
The simples use of the cybercommons API is to simply add two numbers through distrubited message passing and make sure they are
outputted through the framework correctly.
For unit tests we will be implementing simple tests that check for basic functionality of our code when completed such as addition checking. This is the simplest case that can be ran to ensure correct communication with the API

## system tests
For system tests we simply run the api with the help of docker given that we all run on different operating systems as well as other possible users of the api. To ensure the system runs correctly we are able to check docker to make sure all versions:
cybercommons_cybercom_mongo_1  
cybercommons_cybercom_memcache_1 
cybercommons_cybercom_rabbitmq_1 
cybercommons_cybercom_api_1      
cybercommons_cybercom_celery_1
If theses are all running smooth when we run [docker-compose up -d] we know the Django Rest Framework API has been setup correctly

## acceptance tests
For acceptance tests
