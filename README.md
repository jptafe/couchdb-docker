# Couchdb development infrastructure

An exploration of couchdb, node and javascript inside Docker Microservices. 

## Stand up environment 
```
docker-compose up
chrome --disable-web-security --disable-gpu --user-data-dir=/tmp http://frontend.localhost
```
### necessary to turn off CORS, as infrasturcture is not using https which is required for cross-origin sessions

## URLs for each microservice
* http://frontend.localhost/ - html/css/js environment that will use Fetch API to access couchdb 
* http://backend.localhost/ - node application with will proxy couch requests and maintian auth access
* http://couchdb.localhost/ - http endpint with a RESTful webserivice built-in (public data sources only) 

### Deployment
* replace .env file contents with more secure access credintals
* Define https TLD endpints for each microservice
* enable logging
* store/export databases in persistent storage  
