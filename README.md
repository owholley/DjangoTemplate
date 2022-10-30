# Django Template Project

## What the Project Does
This project is a blank Django template project that can be used to quickly start working on a new application, without having to set up user registration and such every single time. It is designed to serve as a jumping off point for Django application development. It's set up to use PostgreSQL. The template includes django-allauth configured from the get go, and includes support for user creation, log-in, log-out, and password reset functionality. Basic static file support is included, and Bootstrap is configured as well.

## Why This Project is Useful
It saves development time having the basic tasks that every web application needs set up from the get go.

## How Users Can Get Started With the Project

## Create A Postgres Database & User

Start Postgres session

`$ sudo -u postgres psql`

Create Database 
 
`postgres=# CREATE DATABASE database-name;`

Create Database User

`postgres=# CREATE USER database-user WITH PASSWORD 'password';`

Configure Settings

`postgres=# ALTER ROLE database-user SET client_encoding TO 'utf8';`

`postgres=# ALTER ROLE database-user SET default_transaction_isolation TO 'read committed';`

`postgres=# ALTER ROLE database-user SET timezone TO 'UTC-5';`

Grant Privileges

`postgres=# GRANT ALL PRIVILEGES ON DATABASE database-name TO database-user;`

Give the user permission to create databases for testing purposes *

`ALTER USER database-user CREATEDB;`

Exit Postgres

`postgres=# \q`

## Create A Python Virtual Environment

If not already installed, install `virtualenv`

`$ sudo -H pip3 install --upgrade pip`

`$ sudo -H pip3 install virtualenv `

Create A `virtualenv' where you keep your Python environments

`$ virtualenv /path/to/environments/environment-name/`

Activate the new `virtualenv`

`$ source /path/to/environments/environment-name/bin/activate/`

Make sure that the prompt in the command line has changed to display the name of the environment to the left of the dollar sign.

`(environment-name)$ `

Install the required Packages

`(environment-name)$ pip install -r requirements.txt`


# Set Up Django Secret Key

Start Django python shell

`(environment-name)$ python manage.py shell`

`>>>import secrets`

`>>>print(secrets.token_urlsafe())`

Copy and paste the secret key into the .env file.

## Where Users Can Get Help With the Project

## Who Maintains and Contributes to the Project
I am the sole maintainer and contributor for the project. It is intended mainly for personal use, but if anybody finds it useful, feel free to shoot me a message with any comments!
