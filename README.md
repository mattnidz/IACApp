# IACApp

## Getting Started

Update the environment variables in *docker-compose.yml*, and then build the images and spin up the containers:


`$ docker-compose up -d --build`

Create the database:
-
`$ docker-compose run web python manage.py create-db`
`$ docker-compose run web python manage.py db init`
`$ docker-compose run web python manage.py db migrate`
`$ docker-compose run web python manage.py create-admin`
`$ docker-compose run web python manage.py create-data`


Access the application at the address [http://localhost:8443/](http://localhost:8443/)

### Testing

Test without coverage:


`$ docker-compose run web python manage.py test`


Test with coverage:


`$ docker-compose run web python manage.py cov`


Lint:


`$ docker-compose run web flake8 project`


## Getting Started - Locally

`$ pip install -r requirements.txt`
`$ python manage.py create-db`
`$ python manage.py db init`
`$ python manage.py db migrate`
`$ python manage.py create-admin`
`$ python manage.py create-data`


`$ python manage.py run`