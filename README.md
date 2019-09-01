# Data Migration Task

## What's provided
### This repository
- You are provided the following
    1. `sabai.sql`
        - This contains all the data collected over the past few years
    2. `data_migration_script.py`
        - You can write your script here!

### Sabai-Backend
- You will need to run this in order to access the back-end API for the later part of your task
- Instructions on setting it up on your local machine are available on the repository

## Task

### Set up the repository into your own machine
1. `git clone <insert https link here>`
    - On the webpage of the repository, find the button labeled **Clone or Download**
    - Copy the link provided
    - Run the above command
2. `git checkout -b <insert your name>-branch`
    - Purpose of this is that you'll have your own branch where you can work in without disturbing other people using the branch
3. `git add *` || `git commit -m <insert comment>` || `git push origin <insert your name>-branch`
    - Your bread and butter whenever you want to make changes to your branch

### Create local databases
1. Using pgAdmin4, create two databases to house the old and new database
2. Name them the following:
    - `Sabai_old` for the old database
        - Using `sabai.sql`, write all the data into this database
    - `Sabai` for the new one
        - This is important since the back-end API will be looking for a database called `Sabai`

### Activating the virtual environment
The very first step is to activate your python virtual environment. This is a **highly** important step so as to clearly separate the dependencies of this project from those that already exist in your own system. Mixing them up can lead to some of your system depencies to malfunction.

We will be using [virtualenv](https://python-guide-ru.readthedocs.io/en/latest/dev/virtualenvs.html) to set up our virtual environment. Run this command if you have yet to install it:

```
$ pip install virtualenv
```

 For setting up the virtual environment for the first time:

```
$ virtualenv venv
```

This creates a /venv folder in your directory. Optimally, you will never need to touch this folder.

Starting the virtual environment:
```
$ source venv/bin/activate
```

This command needs to be run everytime you are working on your project! Or else, you run the risk of installing dependencies/ packages straight into your system.

To ascertain that the virutal environment is active, you should be able to see the word 'venv' appear on the latest line of your terminal/ shell:
```
(venv) (base) Angelico-MBP:sabai_2019 angelico$ 
```

Deactivating the virtual environment:
```
$ deactivate
```

To ensure that it is indeed inactive, the word 'venv' would be gone from the latest line of your terminal/ shell:
```
(base) Angelico-MBP:sabai_2019 angelico$ 
```

### Writing your python script to complete the task:

1. Access contents of old database
2. Clean it up:
    - For each table, make sure that the data structure/ format is the same as the new one
3. By calling the back-end API provided, write the information into the new database

## Dependencies
Make sure that you have the following installed to accomplish the task:
- Python 3
- PostgreSQL
- git

## Helpful programmes
### pgAdmin4
- https://www.pgadmin.org/
- Useful for:
    - Handling and manipulating databases
    - Turning on database

### Postman
- https://www.getpostman.com/downloads/
- Running and testing APIs

## Resources
### Django
- https://www.djangoproject.com/
- This is what our back-end is running on

### Requests
- https://realpython.com/python-requests/
- One of the many libraries that will handle your API requests in your script

### SQL
- https://sqlbolt.com

### git
- https://git-scm.com/docs