## Django - Documentation
![GitHub Logo](https://dl1.cbsistatic.com/i/2019/10/25/3d1ad463-d007-4220-bba7-f22588292444/c1d0cff614ceb63ac7bbf23f9323d189/imgingest-7008501752514407747.png)
 For installing Django in your pc you need to type below command in Command prompt
 ```python 
 pip install Django==3.0.6
 ```
 3.0.6 is the version of Django that installs in your pc
 you have  Django installed already. You can tell Django is installed and which version by running the following command in a shell prompt (indicated by the $ prefix):
```python
$ python -m django --version
```
### Creating a project
  Before getting started with Django you need to auto-generate some code that establishes a Django project– a collection of settings for an instance of Django, including database configuration, Django-specific options and application-specific settings. 
 From command prompt you need get into the directory where you want to create your project by using CD command, Once you reaches the destination you need to type this on your cmd 
 ```python 
 django-admin startproject myfirstproject
 ```
 This creates a new Django project which consistes of below contents in this format
```python
myfirstproject/
    manage.py
    myfirstproject/
        __init__.py
        settings.py
        urls.py
        asgi.py
        wsgi.py
        ```
