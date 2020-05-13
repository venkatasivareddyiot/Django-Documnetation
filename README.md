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
<img src="django flow.png" alt="flow structure"/>




























### Url mappings
url mappings is done by two types
1. By Importing
2. By Using Include 
##### By Importing
Adding urls to urls.py file in project which is main urls file
by importing views from views.py file from app folder
##add an image here
for urls mapping in import format, we need to import all views from myapp(created app name) to the main url.py file
```python 
from myapp import views 
```
by doing this all the methods from views files will be imported to the main URLs file
and in URLs patterns, we need to add every method that we are going to use in views
by the name of path
``` python 
path('index/',views.index,name="index"),
```
form above  **'index/'**   is the url name and  in **views.index** index is the method name in views file in myapp **name: "index"** index is the name  

in views file
##add an image of views file here##
we need to define a method for index when user type */index/* we need to return *Http response* for this we need to import HTTP response library
```pyhon
from Django.http import HttpResponse
```
and then as a response, this method will  return a Http response

``` python
	def index(request):
	return HttpResponse("Welcome to Django")
```
here  **index**  is the method name and **request** is Http request

#### By using Include
urls mapping is also done by using inculde we need to import include function with path
and we need to write a urls.py file inside the myapp 
```python
from django.urls import path,include
```
###add image###
we can link up all the the urls from urls.py file inside the my app by using
```python
 path('myapp/',include('myapp.urls')),
 ```
Here **myapp** is the app name and we are using include which includes all *urls* from myapp.urls.
how many urls we define in ursl.py in my app will be mapped to main urls.py file 

##### urls.py file in myapp
we need to link up all the methods in views so that we need to import them in urls.py file and also the admin urls also
``` python
from django.urls import path
from myapp import views
```
###add image here###
then define paths 
``` python 
path('index/',views.index,name="index"),
```
form above  **'index/'**   is the url name and  in **views.index** index is the method name in views file in myapp **name: "index"** index is the name  

in views file
##add an image of views file here##
we need to define a method for index when user type */index/* we need to return *Http response* for this we need to import HTTP response library
```pyhon
from Django.http import HttpResponse
```
and then as a response, this method will  return a Http response

``` python
	def index(request):
	return HttpResponse("Welcome to Django")
```
here  **index**  is the method name and **request** is Http request
