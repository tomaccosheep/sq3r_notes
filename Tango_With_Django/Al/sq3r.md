## Template

#### Survey
> Skim the article, and then write "done"

#### Question
* Write down some questions that you want to learn from the chapter

#### Read
> Read the chapter and then write "done"

#### Recite
* Take notes on the chapter, write in your own words

#### Review
* Write a review question for yourself

## Chapter 2

#### Survey
> Done

#### Question
* Why install pillow?
* What will it tell me about python3?

#### Read
> Done

#### Recite
You will need to:
* Work with terminal
* Work with python
* Work with pip and venv
* Choose an IDE
* Work with a VCS like Git
* pip is the python package manager


#### Review
* Do you have to manually download and install pillow?
  * No, python's package manager, pip, handles that for you

## Chapter 3

#### Survey
> Done

#### Question
* How do you create a django project?
* How do you create a django app?
* How do you run the server on a different port?

#### Read
> Done

#### Recite
* Use python --version to test the python version
* Run python interactive, import django, and run dango.get\_version() to get the django version
* Start a project with django-admin startproject
  * That creates \_\_init\_\_.py, which indicates that the directory is a python package, settings.py, urls.py, and wsgi.py, which helps you run your server
  * You should also see manage.py, which can be used to run the development server, test the app, run database commands, and poke around in the shell
* python3 manage.py runserver runs the lightweight development server
* Use Ctrl+C to stop the server
* A project = configurations + apps
* Apps make django sites more modular
* Make an app with the command python3 manage.py startapp <appname>
  * That should create \_\_init\_\_.py, admin.py to register models into admin db, apps.py to store app configs, models.py to store the classes that will be used to structure the database, tests.py to store ways to test code, and views.py to store functions that take in requests and return responses, and migrations, which stores database info created from models
* Django follows the MVC pattern
* Register your app in settings.py, in the INSTALLED\_APPS list
* In views, add "from django.http import HttpResponse"
* In urls, import views and path, and add the path to URL patterns
* Import include from django.conf.urls, and make that point at the app urls
* Make a new urls.py in the app, import path and views, and make a new urlpatterns list
* Each urls file strips away from the URL
* URL names are useful for reverse urls

#### Review
* How do you get the version of django installed?
  * In python interactive, import django and run django.get\_version()
* What does startproject create?
  * It creates \_\_init\_\_.py, settings.py, urls.py, wsgi.py
* What does \_\_init\_\_.py do?
  * It lets python know that the directory is a package/module
* What does settings.py do?
  * It remembers the project settings
* What does wsgi stand for?
  * Web server gateway interface

## Chapter 4 (incomplete)

#### Survey
> Done

#### Question
* How do you configure templates and media files in Django?
* Do you have to modify settings.py?
* Can you access stuff in a special URL?

#### Read
> Done

#### Recite
* Django uses the Model Template View structure
* Templates are the static, repetitive parts of websites
* Tango recommends this template structure: <proj_dir>/templates/<app_name>/index.html
* Put the templates directory into the 'DIRS' list in settings.py
* Instead of hardcoding paths, use os.path
* Use {{}} to show a Django template variable
* Tango recommends making a static folder in the project folder
* Change STATIC_DIR in settings.py to point at the folder, using os.path.join(BASE_DIR, 'static')
* Update the list STATICFILES_DIRS
* Always end your urls with a forward slash
* Set STATIC_URL to '/static/'
* You shouldn't deploy with django development server
* Use {% load staticfiles %} and {% static "file" %} to get static files
* Sometimes you have to store dynamic media files, such as a profile picture


#### Review
* 












