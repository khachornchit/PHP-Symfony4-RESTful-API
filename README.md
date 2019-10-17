[![Build Status](https://travis-ci.org/Khachornchit/PHP-Symfony4-RESTful-API.svg?branch=master)](https://travis-ci.org/Khachornchit/PHP-Symfony4-RESTful-API)

# Web API Development using PHP Symfony 4.2
This project demonstrate on how to develop RESTful API application with CRUD method using PHP Symfony 4.2 framework and PHP version 7.2.10, under docker container environment.

So, make sure you have installed docker and docker-compose ready on your environment. Then, you can follow the setup guide step by step.

## Technology Stack
* Linux
* Apache
* MySQL
* PHP 7.2, Symfony 4.2
* Docker
* Travis CI | CICD integration

## Setup Guide
* git clone https://github.com/Khachornchit/PHP-Symfony4-RESTful-API.git
* cd PHP-Symfony4-RESTful-API
* docker-compose build
* docker-compose up -d
* docker-compose exec php bash
	* cd symfony
	* composer install
	* php bin/console doctrine:database:create
	* php bin/console doctrine:migrations:migrate

## phpMyAdmin
The schema symfony_api would be created automatically.
* http://localhost:5033

## API Endpoint
* http://localhost:5031/api

## CRUD
* POST		/users
* GET		/users
* GET		/users/{id}
* PUT		/users/{id}
* DELETE	/users/{id}

## Data
* Example of POST request data
```
{
   "username":"user1",
   "userpassword": "A1234!@#$"
}
```

* Example of POST response data
```
{
   "id": 1,
   "username": "user1",
   "description": "Passed verification."
}
```