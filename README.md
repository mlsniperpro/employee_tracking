### Employee Management System
# employee_tracking
This is a basic employee tracking system written in Django and Python
Python
Django
MYSQL
HTML
Basic Employee Tracking System with a 
      -Login page
      -Employee profile page
      -a page for employees to clock in and out
      -I also want to have different home pages show for employees with different permissions. ie normal users get a page that has a basic screen to go to their profile or to go         to the clock in page and then superusers get directed to a page that has a button to their profile but then also will have a button to approve time off for the normal users.      I have put in a report that has the basics laid out for the program.

### Installation

EMS requires:
- Python 3.7+
- "config.ini" file in "employee-management-system/" folder

You should create superuser account. 
Creating a superuser account using the "python manage.py createsuperuser" command requires entering: username, email and password

Install dependencies, migrate, createsuperuser and run server:

```sh
$ cd employee-management-system/
$ pip install -r requirements.txt 
$ python manage.py migrate
$ python manage.py createsuperuser
$ python manage,py runserver
```

Go to [http://127.0.0.1:8000](http://127.0.0.1:8000)

Run chat server: python manage.py run_chat_server


### Throubleshooting:

- SyntaxError in compability.py

 try:                                                     # pragma: no cover 

     asyncio_ensure_future = asyncio.ensure_future        # Python ≥ 3.5 

 except AttributeError:                                   # pragma: no cover 

     asyncio_ensure_future = getattr(asyncio, 'async')    # Python < 3.5 
     