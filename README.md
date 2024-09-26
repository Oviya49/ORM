# Ex02 Django ORM Web Application
## Date: 26/09/2024

## AIM
To develop a Django application to store and retrieve data from a bank loan database using Object Relational Mapping(ORM).

## ENTITY RELATIONSHIP DIAGRAM
![image](https://github.com/user-attachments/assets/564b4802-4007-4111-b12f-04eefc0a8710)



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
## Models
```
from django.db import models
from django.contrib import admin
class Bank(models.Model):
    customer_id = models.IntegerField(primary_key=True)
    customer_name = models.CharField(max_length=50)
    account_type = models.CharField(max_length=50)
    loan_amount = models.DecimalField(max_digits=10, decimal_places=2)  
    monthly_interest = models.DecimalField(max_digits=5, decimal_places=2)  
    due_date = models.DateField()

    def __str__(self):
        return self.customer_name  # Optional, for better representation in admin or shell

class BankAdmin(admin.ModelAdmin):
    list_display = ('customer_id', 'customer_name', 'account_type', 'loan_amount', 'monthly_interest', 'due_date')
admin.site.register(Bank, BankAdmin)
```
## Admin
```
from django.contrib import admin
from .models import Bank, Loandetails

admin.site.register(Bank)
admin.site.register(Loandetails)
```


## OUTPUT

![Screenshot 2024-09-26 231832](https://github.com/user-attachments/assets/d8b372a4-fd18-4212-bc83-4e87bb29b520)
![Screenshot 2024-09-26 231903](https://github.com/user-attachments/assets/5dabab61-37b4-4efa-92a4-970038c0ad73)




## RESULT
Thus the program for creating a database using ORM hass been executed successfully
