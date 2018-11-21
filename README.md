

-----------------------------------------------------
|                                                   |
|        Full Stack Frameworks with Django          |
|                                                   |
-----------------------------------------------------

Table of Content

1. Beginning Django
1.1. Hello Django
1.2. Testing Django
2. Development
2.1. The Heroku Platform
2.2. Making Our Code Deployment Ready
2.3. Deploying Our Project
2.4. Environments, Automation & Security
3. Authentication & Authorisation
3.1. Getting Set Up
3.2. Logging Out
3.3. Creating Login Functionality
3.4. Authorisation
3.5. User Registration & Profiles
3.6. Password Reset
3.7. Custom Authentication
4. Bootstrapping A Django Project
4.1. Styling A Django Project
5. Blog All About It
5.1. Set Yourself Up For Success
5.2. Create Models, Views And URLs
5.3. Create HTML templates and CSS styles
5.4. Let's Go Live
6. Putting It All Together I ECommerce Mini Project
6.1. Products and a Shopping Cart
6.2. Finding and Purchasing Products
6.3. Hosting your E-commerce web app
7. Milestone Project
7.1. Full Stack Framworks with Django Milestone Project
7.2. Congratulations! You've just completed Fullstack Frameworks with Django
7.3. Even Bigger Congratulations! You are ready to complete the course!

1 Beginning Django
1.1. Hello Django
1.1.1. Beginning Django
-----------------------------------------------------

sudo pip3 install django==1.11

django-admin startproject django_todo .

python3 manage.py runserver $IP: $C9_PORT

/django_todo/settings.py/
ALLOWED_HOSTS = ['django-rayzhu247.c9users.io']

cmd s

refresh Django

copy
python3 manage.py runserver $IP:$C9_PORT

go to setting to choose show home in favourite

/.bash_aliases/

alias="python3 manage.py runserver $IP:$C9_PORT"

cmd s

ctrl c > exit (to open a new terminal to activate alias)

------------------------------------
1.1.2 URLs
------------------------------------

django-admin startapp todo

/todo/views.py/
from django.shortcuts import render, HttpResponse

# Create your views here.
def say_hello(request):
    return HttpResponse("Hello World")
    
/django_todo/urls.py/
from todo.views import say_hello

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^$', say_hello)
]

^message$
message$
^messagepoerijpoiwrp

------------------------------------
1.1.3 Templates
------------------------------------
/todo/templates/todo_list.html

/todo/views.py

....
def get_todo_list(request):
    return render(request, "todo_list.html")

/django_todo/urls.py
from todo.views import get_todo_list

urlpatterns = [
    url(r'^admin/', admin.site.urls),
    url(r'^$', get_todo_list)
]

/django_todo/settings.py
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'todo',
]

run

go to the url viewpoint, todo_list.html will show.

delete the say_hello function from the urls.py

------------------------------------
1.1.4 Admin
------------------------------------

sqlite3 db.sqlite
> .tables
> select * from django_migrations;
> .quit

python3 manage.py migrate

sqlite3 db.sqlite
> .tables
> select * from django_migrations;
> .headers on
> select * from django_migrations;
> .mode column
> select * from django_migrations;
> .talbes
> .quit

python3 manage.py createsuperuser
admin
admin@example.com
jiahuizhu
jiahuizhu
sqlite3 db.sqlite
> .tables
> select * from auth_user;
> .quit

run
https://django-rayzhu247.c9users.io/admin
admin
jiahuizhu

show Home in Favorites
create a new file:
/.sqliterc
.headers on
.mode column

sqlite3 db.sqlite
> .tables
> select * from auth_user;
> .quit


------------------------------------
1.1.5 Models
------------------------------------



