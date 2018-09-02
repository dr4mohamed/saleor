release: heroku config:set DISABLE_COLLECTSTATIC=1
release: python manage.py migrate --no-input
web: uwsgi saleor/wsgi/uwsgi.ini
celeryworker: celery worker -A saleor.celeryconf:app --loglevel=info -E
