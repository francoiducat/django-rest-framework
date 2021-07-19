
# API with Django Rest Framework

Simple API to allow admin users to view and edit the users and groups in the system.

## Create the project directory
mkdir API
cd API

## Create a virtual environment to isolate our package dependencies locally
python3 -m venv env
source env/bin/activate  # On Windows use `env\Scripts\activate`

## Install Django and Django REST framework into the virtual environment
pip install django
pip install djangorestframework

## Set up a new project with a single application
django-admin startproject tutorial .  # Note the trailing '.' character
cd tutorial
django-admin startapp quickstart
cd ..

## Sync database

python manage.py migrate

## Create an initial user

python manage.py createsuperuser --email admin@example.com --username admin
