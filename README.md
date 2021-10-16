# DjangoTelegramBotTemplate
Django Telegram Bot Template for the initial setup and start of writing the project

## Setting up a virtual environment
Virtual environments are a powerful and convenient tool for isolating programs from each other and from the system (your local computer/laptop). Most often, it is more convenient not to install some package on a computer as a module, but rather install it in your virtual environment, which will allow you to greatly simplify the work when turning the project to third-party resources.

Install **poetry** to manage the virtual environment

**Poetry** is packaging and dependency management made easy.

At the moment, virtualenv is already an outdated and impractical way to install and manage dependencies.
```shell script
https://python-poetry.org/docs/#installation
```

After installing poetry, you need to initialize poetry to use it as a virtual environment

```shell script
poetry init
```

Poetry will start asking you some parameters to configure your own virtual environment dependency package. As an example, I will enter my data, you can enter those that you deem necessary
```shell script
Package name [djangotelegrambottemplate]: DjangoTelegramBotTemplateDependences
Version [0.1.0]: (PRESS ENTER)
Description []: (PRESS ENTER)
Author [ronnycray <chayka1998A@yandex.ru>, n to skip]: (PRESS ENTER)
License []: (PRESS ENTER)
Compatible Python versions [^2.7]: ^3.9
Would you like to define your main dependencies interactively? (yes/no) [yes] no
Would you like to define your development dependencies interactively? (yes/no) [yes] no
Do you confirm generation? (yes/no) [yes] yes
```
The pyproject.toml file will appear in the project folder

The pyproject.toml file contains a description of your Poetry project - name, description, repository used, project dependencies, etc. With it, it is easy to organize the dependencies of your project (pyproject.toml can be called the successor of the outdated one requirements.txt ).

To use our initialized virtual environment now, we will set the primary settings from pyproject.toml
```shell script
poetry install
```

After that, you should have such an entry
```shell script
Using python3 (3.9.5)
Creating virtualenv djangotelegrambottemplatedependences-NvI0YBOI-py3.9 in /Users/aleksandrchaika/Library/Caches/pypoetry/virtualenvs
Updating dependencies
Resolving dependencies... (0.1s)

Writing lock file
```
Instead */Users/aleksandrchaika/Library/Caches/pypoetry/virtualenvs* you will have your own path to the virtual environment

For each operating system, the paths where all your created virtual environments are stored are different. Here is an example
```buildoutcfg
for Windows – C:\Users\<username>\AppData\Local\pypoetry\Cache\virtualenvs;
for Linux – ~/.cache/pypoetry/virtualenvs;
for macOS – ~/Library/Caches/pypoetry/virtualenvs.
```

Next, we need to use our created virtual environment to completely isolate ourselves from the system and install the necessary modules into the project without any problems
```shell script
source /Users/aleksandrchaika/Library/Caches/pypoetry/virtualenvs/djangotelegrambottemplatedependences-NvI0YBOI-py3.9/bin/activate
```
After that you should have something like
```shell script
(djangotelegrambottemplatedependences-NvI0YBOI-py3.9) ➜ DjangoTelegramBotTemplate git:(main) ✗
```

We have set up a virtual environment and now we can proceed to setting up the project. Congratulations 😂. If you thought what kind of shit this is 💩, believe me, it will help you a lot in the future in creating projects.

## Installing dependencies
Let's install Django and the library for working with Telegram
```shell script
poetry add Django==3.1 pyTelegramBotApi
```

## Settings Django project
Django is a free and free framework for web applications written in Python. A framework is a set of components that help you develop websites quickly and simply.

First we need to create a Django project
```shell script
django-admin startproject backend
```

**backend** - our main project directory in which the program code will be
Introduction | Documentation | Poetry -.. python-poetry.org
written

Project created by django consists of applications that we create. Let's create a project that will contain an SQLite database and an administrative panel, which we will expand further

Let's go to the project folder
```shell script
cd backend/
```

Our project contains the main project folder, which has the same name as our backend project. There is also a file manage.py which is the main script to run our application
```shell script
backend manage.py
