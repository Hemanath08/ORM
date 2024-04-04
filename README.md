# Ex02 Django ORM Web Application
## Date: 

## AIM
To develop a Django application to store and retrieve data from a Book database using Object Relational Mapping(ORM).

## DESIGN STEPS

### STEP 1:
Clone the problem from GitHub

### STEP 2:
Create a new app in Django project

### STEP 3:
Enter the code for admin.py and models.py

### STEP 4:
Execute Django admin and create details for 10 books

## PROGRAM

models.py

from django.db import models

class Student(models.Model):
    stdid=models.IntegerField()
    stdname=models.CharField(max_length=30)
    dept=models.CharField(max_length=20)
    cgpa=models.FloatField()
    aadhar=models.BigIntegerField(null=True)

admin.py

from django.contrib import admin

from .models import Student
admin.site.register(Student)


class Student(admin.ModelAdmin):
    list_display=('Stdid','Stdname','Dept','Cgpa','Aadhar')

## OUTPUT

![Output](https://github.com/Hemanath08/ORM/assets/151807176/de5eb750-d728-4b39-9690-66b664068491)


## RESULT
Thus the program for creating a database using ORM hass been executed successfully
