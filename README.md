# Ex02 Django ORM Web Application
## Date: 14-03-2024

## AIM
To develop a Django application to store and retrieve data from a Train booking database using Object Relational Mapping(ORM).

## Entity Relationship Diagram

![Screenshot 2024-03-19 104653](https://github.com/Beatricethomas/ORM/assets/140035214/a313b3d3-64de-4608-8d80-18044aa4f93f)


## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 trains

## PROGRAM

```
admin.py 

from django.contrib import admin
from .models import railway,railwayAdmin
admin.site.register(railway,railwayAdmin)


models.py

from django.db import models
from django.contrib import admin
class railway (models.Model):
    train_code=models.CharField(max_length=20,help_text="railway train_code")
    train_name=models.CharField(max_length=100)
    start_time=models.IntegerField()
    End_time=models.IntegerField()
    start_station_code=models.IntegerField()
    end_station_code=models.IntegerField()
     
class railwayAdmin(admin.ModelAdmin):
    list_display=('train_code','train_name','start_time','End_time','start_station_code','end_station_code',)

```

## OUTPUT

![alt text](<Screenshot 2024-03-14 213732.png>)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
