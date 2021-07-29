web: gunicorn harvestify.wsgi --timeout 120 --keep-alive 5 --log-level debug
python manage.py collectstatic --noinput
manage.py migrate
