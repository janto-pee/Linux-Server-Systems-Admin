# Python and Django Rest Framework With Terraform
## Table of Contents

1. [What is DRF?](#what-is-nextjs)
1. [Introduction](#introduction)
1. [Project Initialization](#project-setup)
1. [Folder Structure](#folder-structure)
1. [Postgresql Setup](#git-setup)
1. [Configure GDAL](#code-formatting-and-quality-tools)
1. [Set Env Variables](#git-hooks)
1. [Create Super User](#vs-code-configuration)
1. [Create Model](#debugging)
1. [Serializers](#directory-structure)
1. [Views](#adding-storybook)
1. [Setup Account](#creating-a-component-template)
1. [Account Serializer](#using-the-component-template)
1. [Error Handling](#adding-a-custom-document)
1. [Package](#adding-layouts)
1. [Terraform](#deployment)
1. [Deployment](#next-steps)
1. [Wrapping Up](#wrapping-up)

## What is Django Rest Framework?

_Django REST framework abbreviated as "DRF" is a powerful and flexible toolkit for building Web APIs. Although DRF and Django have a lot of similarities, they are suited for differentpurposes. 

Django is a high-level Python web framework that encourages rapid development and clean, pragmatic design. Built by experienced developers, it takes care of much of the hassle of web development, so you can focus on writing your app without needing to reinvent the wheel. It’s free and open source

DRF is a powerful and flexible toolkit used to build Web APIs on top of Django. While Django deals with the overall web application, including both frontend and backend components, DRF is used to build RESTful APIs that allow interaction and communication between different software components. 

With DRF, it’s easier to design the CRUD operations and use a Django Server as a REST API. Django Rest framework leverages Django’s capabilities to facilitate the development of scalable, maintainable, and secure APIs. It adheres to Django’s principles like DRY (Don’t Repeat Yourself) and emphasizes reusability and modularity.

## Introduction

This project documentation does not replace the official documentation, which is absolutely great. Therefore, I highly encourage you to go through at least the [DRF features](https://www.djangoproject.com/) section before you use this project, so you'll be familiar with the terminology and tools and some of the features they provide that are similar.

Please review the table of contents to get an idea of each of the topics we will be touching in this extensive tutorial. 

Now, with all that said, if you are ready, let's jump in!

## Project Initialization

We'll begin by creating a folder for the project.

```bash
mkdir indeedjob
# npx create-next-app --ts nextjs-fullstack-app-template

# cd nextjs-fullstack-app-template
```
Lets install the virtualenv tool to create an isolated Python environments. 
```bash
python -m pip install --user virtualenv
python -m virtualenv --help
```
We will create and activate a virtual environment using the installed tool;
```bash
virtualenv env
source env/scriptsactivate
```
we will need to install django, django-rest-framework, django-filters as well as other programs in the requirements.txt
```
django
djangorestframework
djangorestframework-simplejwt
django-storages
django-cors-headers
django-dotenv
django-filter
gunicorn
geocoder
whitenoise
boto3
psycopg2
dj-database-url
```

Now install

```bash
pip install -r requirements.txt
```


## Folder Structure

We would like for this project to host both the frontend and backend of this project.

- `mkdir frontend` - will use typescript, next.js, react, tailwindcss
- `mkdir backend`  - Will use python, django-rest-framework

Now lets proceed with the `backend` :

```
cd backend
django-admin startproject backend .
django-admin manage.py startapp job
django-admin manage.py startapp account
```

The `django-admin startproject backend .` helps to auto-generate some code that establishes a Django project – a collection of settings for an instance of Django, including database configuration, Django-specific options and application-specific settings. The `django-admin manage.py startapp job` is a command-line utility for administrative tasks. 


## Database (Postgresql) Setup

Make sure you have a postgres database set up already, now go to `backend/settings.py` and add the following
```

```
