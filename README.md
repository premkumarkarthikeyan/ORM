# Django ORM Web Application

## AIM
To develop a Django application to store and retrieve data from a database using Object Relational Mapping(ORM).

## Entity Relationship Diagram
![Entity Relationship Diagram](./prem.png)

## DESIGN STEPS

### STEP 1:
create a migration file that contains code for the database schema of a model in my app

### STEP 2:
Apply all the migrations to the myapp

### STEP 3:
create users in the Employee link under'myapp'

## PROGRAM
```
models.py
from django.db import models
from django.contrib import admin
class Employee(models.Model):
    eid=models.CharField(primary_key="eid",max_length=20,help_text="Employee ID")
    name=models.CharField(max_length=100)
    salary=models.IntegerField()
    age=models.IntegerField()
    email=models.EmailField()
class EmployeeAdmin(admin.ModelAdmin):
    list_display=('eid','name','salary','age','email')

admin.py
from django.contrib import admin
from.models import Employee ,EmployeeAdmin
admin.site.register(Employee,EmployeeAdmin)
```

## OUTPUT
![OUTPUT](./123.png)

## RESULT
program Executed sucessfully