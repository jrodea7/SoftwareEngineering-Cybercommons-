# Cybercommons

## What is it?
Cybercommons is a web application that allow for storage of catalogs and other types of data onto a database. Our sponsor, Tyler Pearson, essentially describes Cybercommons as a Django REST framework API. Visit the Repo here -> https://github.com/cybercommons

## Technologies Used
Cybercommons makes use of many different technologies to get it running. For starters, the application uses Docker and Docker-Compose to built and run quickly on one's own local machine. Docker makes it easy to build the application without the issue of "well it works on my machine." The two languages used in Cybercommons are JavaScript and Python3. Django is another technology used for easy Python Web Development. MongoDB is an important technology used concerning with the storage of catalogs and data. All data stored in Cybercommons is stored as a JSON document format. Celery and RabbitMQ helps with messaging passing and constantly looking for new work to perform in Cybercommons to keep it running smoothly.

## Tasks Assigned
Our sponsor, Typer Pearson, had a good working system. He wanted us to add additional features to the application such as:
1) SSL Creation - current config with preset SSL.
2) NGINX Config
3) JWT Pay-Load
4) Integration with Kubernetes (!!! In progress !!!)

## What We Learned
We learned about the technologies involved and experimented with it. We feel confident in using Docker and Docker-Compose in creating Makefiles and docker-compose.yml to deploy services. We feel confident in Python3 coding along with JavaScript. We did not make a huge contribution to Cybercommons but we did bring up issues that occur when deploying it to our sponsor. The issue was port errors that occur and he thanked us for letting him know.

## Requirements

* Docker
* Docker Compose
    * `pip install docker-compose`
* GNU Make or equivalent

## Testing 
Reference file: Testing.md and testing branch for further information

## Deployment
1. Edit values within dc_config/cybercom_config.env  (not required)
2. Initialize database and generate internal SSL certs

        $ make init

3. Build and Deploy

        $ make build
        $ make run

4. API running http://localhost:8080
    * Username: admin
    * Password: admincybercom

5. Kill

        $ make stop

If problems reference: (https://github.com/oulib-datacatalog/cybercommons)

## Installation (version 2)

** Requires Docker and CookieCutter (pip install cookiecutter) **

1. Run the following to create file structure => cookiecutter https://github.com/cybercommons/cybercom-cookiecutter.git
2. Add aauthor and application title to your application
    author [Some Guy]:
    application_title [Some Application]:
3. Add application name:
    application_short_name [someapp]:
4. Build Docker container with:
    cd someapp/api_code
    docker build -t api .
    cd ..
5. Run the application:
  ./run/cybercom_up
