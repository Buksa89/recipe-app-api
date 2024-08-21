docker-compose run --rm app sh -c "python manage.py collectstatic"

linting with docker:
- install flake8 package
- run it through docker-compose:
    docker-compose run --rm app sh -c "flake8"

testing with docker:
    docker-compose run --rm app sh -c "python manage.py test"

create django app:
    docker-compose run --rm app sh -c "django-admin startproject app ."
