# Sample Microservice Application

Geek's Movie Shop (former Stan's Robot Shop) is a sample microservice application you can use as a sandbox to test and learn containerised application orchestration and monitoring techniques. It is not intended to be a comprehensive reference example of how to write a microservices application, although you will better understand some of those concepts by playing with it. To be clear, the error handling is patchy and there is not any security built into the application.

Forked from the original [Robot-Shop](https://github.com/instana/robot-shop) repository, by Instana.

This sample microservice application has been built using these technologies:
- NodeJS ([Express](http://expressjs.com/))
- Java ([Spark Java](http://sparkjava.com/))
- Python ([Flask](http://flask.pocoo.org))
- Golang
- PHP (Apache)
- MongoDB
- Redis
- MySQL
- RabbitMQ
- Nginx
- AngularJS

# (optional) use an EC2 instance

Setup a free-tier EC2 Amazon Linux instance with 24Gb storage and follow the instructions in *TRAINING_GUIDE.sh* to have a working Docker enviroment you can play with. Don't forget to open port 8888 to the world and change the *PUBLIC_URL* to the EC2 instance DNS.

# Docker Deployment

## Setup your .env file
Create a .env file from env.template and set these variables:
- GITHUB_USER=
- GITHUB_USER_NAME='FIRST_NAME LAST_NAME'
- GITHUB_USER_EMAIL=
- GITHUB_REPO=latam-newr-training

- DOCKERHUB_USER=
- TAG=latest

- PUBLIC_URL=http://YOUR_INSTANCE_DNS:8888

- NEW_RELIC_LICENSE_KEY=
- CLUSTER_NAME=local

- NEW_RELIC_BROWSER_LICENSE_KEY=
- NEW_RELIC_BROWSER_APPLICATION_ID=

## Build

`docker-compose build`

## Run

`docker-compose up -d`

There is a loader container that produces some backend traffic.

## Access the Store
The store front is available on [http://YOUR_INSTANCE_DNS:8888](http://localhost:8888)

## Stop

`docker-compose down`
