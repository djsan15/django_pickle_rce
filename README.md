# Django Pickle RCE
A simple POC with a vulnerable django app

## Setup
- The django version is 1.11.29
- The following settings make it vulnerable:
  ```
  SESSION_ENGINE = 'django.contrib.sessions.backends.signed_cookies'
  SESSION_SERIALIZER = 'django.contrib.sessions.serializers.PickleSerializer'
  ```
## How to run
- On 1 terminal, run the server using `python3 manage.py runserver`
- On the other terminal, run the exploit using `python3 exploit.py`
- You should see the commands getting executed on the terminal running the django server.
