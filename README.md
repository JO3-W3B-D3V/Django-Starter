# Django Experiment

This repository is nothing more than me tinkering with some Python solution(s).

## Local Environment & Setup
To get this application up & running from nothing, you'll want to run the following commands. Keep in mind this was done on a Windows 10 machine, the commands will *generally* differ for a Mac or Linux machine, though it's the same idea(s).

```batch
python3 -m venv venv
venv\Scripts\activate.bat
pip install Django 
django-admin startproject experiment 
move "%CD%\experiment\manage.py" "%CD%"
move "%CD%\experiment\experiment\*" "%CD%\experiment"
rmdir "%CD%\experiment\experiment"
python manage.py runserver
```
You can now visit [this URL](http://localhost:8000/) to make sure that it's working.

### Dependencies 
If you're lazy like myself, you'll want to generate a list of the installations, to do so all you need to do is write the following command(s):

```batch 
venv\Scripts\activate.bat
pip3 freeze > requirements.txt
```

When it comes to installing these dependencies at a later date, all you'll need to do is the following: 

```batch
venv\Scripts\activate.bat
pip3 install -r requirements.txt
```