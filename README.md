# SWAPI
## The Star Wars API

## NO LONGER MAINTAINED!

If you rely on this project for your own tools - then please fork and spin up your own instance. It's a pretty simple project, and the Makefile will take you a long way.

If you are looking for an API to play with to learn about APIs, then I recommend [https://pokeapi.co](https://pokeapi.co).

```shell
install:
	pip install -r requirements.txt

build:
	python manage.py migrate
	python manage.py createsuperuser

load_data:
	python manage.py loaddata planets.json
	python manage.py loaddata people.json
	python manage.py loaddata species.json
	python manage.py loaddata transport.json
	python manage.py loaddata starships.json
	python manage.py loaddata vehicles.json
	python manage.py loaddata films.json

serve:
	python manage.py runserver

dump_data:
	python manage.py dumpdata resources.planet > resources/fixtures/planets.json --indent 4
	python manage.py dumpdata resources.people > resources/fixtures/people.json --indent 4
	python manage.py dumpdata resources.species > resources/fixtures/species.json --indent 4
	python manage.py dumpdata resources.starship > resources/fixtures/starships.json --indent 4
	python manage.py dumpdata resources.vehicle > resources/fixtures/vehicles.json --indent 4
	python manage.py dumpdata resources.transport > resources/fixtures/transport.json --indent 4
	python manage.py dumpdata resources.film > resources/fixtures/films.json --indent 4


drop_db:
	python manage.py flush

test:
	python manage.py test


clear_cache:
	python manage.py clear_cache

```