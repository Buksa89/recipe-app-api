docker-compose run --rm app sh -c "python manage.py collectstatic"
docker-compose run --rm app sh -c "
docker-compose build
docker-compose up



linting with docker:
- install flake8 package
- run it through docker-compose:
    docker-compose run --rm app sh -c "flake8"

testing with docker:
    docker-compose run --rm app sh -c "python manage.py test && flake8"

create django app:
    docker-compose run --rm app sh -c "django-admin startproject app ."

python3 -m venv .venv
python3 -m pip install -r requirements.txt
source .venv/bin/activate