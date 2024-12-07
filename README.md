# Ex.06 Book Front Cover Page Design
# Date:
# AIM:
To design a book front cover page using HTML and CSS.

# DESIGN STEPS:
## Step 1:
Create a Django Admin project.

## Step 2:
Create an app in the Django interface.

## Step 3:
Create a folder named 'static' in the app folder.

## Step 4:
Create a new HTML file in the static folder.

## Step 5:
Write the HTML code with relevant CSS properties.

## Step 6:
Choose the appropriate style and color scheme.

## Step 7:
Insert the images in their appropriate places.

## Step 8:
Publish the website in the LocalHost.

# PROGRAM:
```
<html>
    <head>
        <title>BOOK FRONT COVER PROJECT</title>
        {% load static %}
        <style>
            body{
                background-repeat: no-repeat;
                margin-left:30%;
                margin-top:20%;
                background-position: 350px;
            }
            #line1 {
                color: rgb(184, 184, 184);
                position: absolute;
                top: 180px;
                left: 620px;
                font-size: 14px;
                font-family:"Pacifico", serif;
                font-style: normal ;
                align-items: center;
            }
            #line2 {
                color: rgb(184, 184, 184);
                position: absolute;
                top: 230px;
                left: 570px;
                font-size: 14px;
                font-family:"Pacifico", serif ;
                font-style: normal ;
            }
            #author {
                color: rgb(173, 182, 50);
                top: 900px;
                left: 470px;
                font-size:50px;
                position: absolute;
                font-family: "Russo One", sans-serif;
                font-style: normal;   
            }
            #edition {
                color: aliceblue;
                left: 530px;
                top: 890px;
                position: absolute;
                font-style: oblique;
                font-size: 20px;

            }
             #lotus{
                position: absolute;
                left: 500px;
                top: 300px;
             }    
             
        </style>
    </head>
    <body style="background-image: url('{%static 'bookcover.jpg'%}');">
        
        <div id="line" >
        <div id="author">
            <h1>RINA KENT</h1>
        </div>
        <div id="line1">
            <h1>I'M TAKEN BY A</h1>
        </div>
        <div id="line2">
            <h1>BEAUTIFUL NIGHTMARE</h1>
        </div>
        <div id="edition">
            <h1>LEGACY OF GODS</h1>
        </div>
        <div id="lotus">
            {% load static %}
            <img src="{% static '[removal.ai]_134ee9e1-aa6d-4b07-b1a4-a35153cdd700-flower.png' %}" width="460px" alt="">
        </div>

        </div>
    </body>
```
VIEWS.PY:
```
from django.shortcuts import render
def book(request):
    return render(request,'BOOK.html')
```
SETTINGS.PY
```
"""
from pathlib import Path
import os

BASE_DIR = Path(__file__).resolve().parent.parent

DEBUG = True

ALLOWED_HOSTS = []

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'bookex2',
]

MIDDLEWARE = [
    'django.middleware.security.SecurityMiddleware',
    'django.contrib.sessions.middleware.SessionMiddleware',
    'django.middleware.common.CommonMiddleware',
    'django.middleware.csrf.CsrfViewMiddleware',
    'django.contrib.auth.middleware.AuthenticationMiddleware',
    'django.contrib.messages.middleware.MessageMiddleware',
    'django.middleware.clickjacking.XFrameOptionsMiddleware',
]

ROOT_URLCONF = 'ex2.urls'

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
                'django.contrib.messages.context_processors.messages',
            ],
        },
    },
]

WSGI_APPLICATION = 'ex2.wsgi.application'
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': BASE_DIR / 'db.sqlite3',
    }
}

AUTH_PASSWORD_VALIDATORS = [
    {
        'NAME': 'django.contrib.auth.password_validation.UserAttributeSimilarityValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.MinimumLengthValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.CommonPasswordValidator',
    },
    {
        'NAME': 'django.contrib.auth.password_validation.NumericPasswordValidator',
    },
]

LANGUAGE_CODE = 'en-us'

TIME_ZONE = 'UTC'

USE_I18N = True

USE_TZ = True

STATIC_URL = 'static/'

DEFAULT_AUTO_FIELD = 'django.db.models.BigAutoField'
```
URLS.PY
```
from django.contrib import admin
from django.urls import path,include
from bookex2 import views
urlpatterns = [
    #path('admin/', admin.site.urls),
    path('book',views.book)
]
```
# OUTPUT:
![image](https://github.com/user-attachments/assets/1fcafebe-b073-4ca5-9822-8d803a23232d)
# RESULT:
The program for designing book front cover page using HTML and CSS is completed successfully.
