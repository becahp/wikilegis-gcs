# Wikilegis

Sistema de Consultas Públicas baseado no Wikilegis da Câmara de Deputados do Brasil.

# Requirements

Os mesmos de https://github.com/caiquepereira/wikilegis-gcs.

* Python 2.7.x

# Instalation

```bash
$ git clone https://github.com/becahp/wikilegis-gcs.git
$ cd wikilegis
$ pip install -r requirements.txt
```

## Database and superuser setup

```bash
$ ./manage.py migrate
$ ./manage.py createsuperuser
```

## Running the development server

```bash
$ ./manage.py runserver
```

## Running the development server on Vagrant

```bash
$ ./manage.py runserver 0.0.0.0:8000
```

## Opening the Vagrant server locally

```bash
$ http://localhost:8000
```



# Customizing settings

To customize some wikilegis settings, create the file `settings.ini` on `./wikilegis/settings/`. The availables parameters are:

```bash

[settings]

# Application settings
API_KEY = api_key
SECRET_KEY = secret_key
DEBUG = 1 # True
ALLOWED_HOSTS = *
DATABASE_ENGINE = sqlite3 # postgresql, mysql, sqlite3, oracle
DATABASE_NAME = db.sqlite3
DATABASE_USER
DATABASE_PASSWORD
DATABASE_HOST
DATABASE_PORT

# Authentication settings
LOGIN_URL = /accounts/login/
LOGIN_REDIRECT_URL = /
AUTH_USER_MODEL = auth2.User

# Email settings
EMAIL_HOST = localhost
EMAIL_PORT = 587
EMAIL_HOST_USER
EMAIL_HOST_PASSWORD
EMAIL_USE_TLS
DEFAULT_FROM_EMAIL

# Locale settings
LANGUAGE_CODE = pt-br
TIME_ZONE = America/Sao_Paulo

# Staticfiles settings
STATIC_URL = /static/
MEDIA_URL = /media/

# Facebook Settings
SOCIAL_AUTH_FACEBOOK_KEY = facebook_key
SOCIAL_AUTH_FACEBOOK_SECRET = facebook_secret

# Google Settings
SOCIAL_AUTH_GOOGLE_OAUTH2_KEY = google_key
SOCIAL_AUTH_GOOGLE_OAUTH2_SECRET = google_secret
```

# Admin interface

If everything went right, the admin interface is now available at: http://127.0.0.1:8000/admin. You can log in using the superuser credentials you just created and manage all kinds of contents. Once you're done managing your site, go visit the main page at http://127.0.0.1:8000/.


# Translating

TODO: Instructions to use Transifex to translate this.
