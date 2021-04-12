# Couchdb development infrastructure

An exploration of couchdb, node and javascript inside Docker Microservices. This project forms the basis for an investigation of nosql without that pesky CORS getting in the way. 

## Stand up environment 
```
cp env_example .env
docker-compose up
firefox http://localhost/frontend/
```
### NOTE the trailing slash 

## URLs for each microservice
* http://localhost/frontend/ - html/css/js environment that will use Fetch API to access couchdb 
* http://localhost/backend/index.js - node application with will proxy couch requests and maintian auth access
* http://localhost/couchdb/\_utils/ - http endpint with a RESTful webserivice built-in 

## FILES in this project
* ./frontend - Vanilla JS experience
* ./backend - Vanilla Node JS experience
* ./couchdb - configuration and data for persistence

## TODO build as far as possible a JavaScript UI that:
* Build shopping catalog with products and categories
* Build a shopping cart experience that stores product choices on a per-user basis
* Build a login/registration system that can attach to the cart document in couchdb
* Build a checkout model that will attach invoices of cart items and flush cart when done

## Possible Gotchyas
* frontend container has no npm executable, may need this just like backend...

[![Try in PWD](https://raw.githubusercontent.com/play-with-docker/stacks/master/assets/images/button.png)](https://labs.play-with-docker.com/?stack=https://raw.githubusercontent.com/jptafe/couchdb-docker/main/docker-compose.yml)
