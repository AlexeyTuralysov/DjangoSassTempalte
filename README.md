````
pip install libsass django-sass-processor
````

# settings.py
````
#settings.py
# Application definition

INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',

    'sass_processor',
    'myapp',
]

STATIC_URL = 'static/'
STATIC_ROOT = BASE_DIR / 'static'
SASS_PROCESSOR_ROOT = STATIC_ROOT
````
# myapp/index.html

````
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
    {% load sass_tags %}
    <link href="{% sass_src 'myapp/css/mystyle.scss' %}" rel="stylesheet" type="text/css" />


</body>
</html>
````