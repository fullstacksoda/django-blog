# django-blog
a simple blog made with Django.

To setup the blog, first ensure that you have Python and the latest Django version installed.

Clone the repo, navigate to the directory then initialise the first migrations with

```
python manage.py migrate
```

Create your user with

```
python manage.py createsuperuser
```

Then start the server with 

```
python manage.py runserver
```

navigate to 127.0.0.1:8000/admin and log in. You can see that you will be able to create posts and comments from the dashboard.

navigate to 127.0.0.1:8000/blog to see posts listed and you can visit the post to add/view comments

If you want to enable the share by email feature, you will need to edit settings.py and replace 

```python
EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'
```

with your email details like so:

```python
EMAIL_HOST = 'your email host smtp'
EMAIL_HOST_USER = 'your email address'
EMAIL_HOST_PASSWORD = 'your email password'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
```

![Example blog](https://raw.githubusercontent.com/fullstacksoda/django-blog/main/Screenshot%20from%202023-01-05%2013-27-02.png)
