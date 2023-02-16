# YaMDb

Workflow status

![example workflow](https://github.com/IskanderRRR/yamdb_final/actions/workflows/yamdb_workflow.yml/badge.svg)

### About:
The YaMDb is a review-aggregation project for film, television, book, music. The YaMDb collect online reviews from users. The users upload their reviews to the movie(TV-show,book,music) page on the website.The YaMDb keeps track of all the reviews counted for each film. An average score on a 0 to 10 scale is also calculated.

### Applied technologies:
- Python
- Django
- Django Rest Framework
- Simple-JWT
- GIT
- SQLite

### User Roles
- Anonymous - can view descriptions of works, read reviews and comments.

- Authenticated user (user) - can read everything, like Anonymous, can additionally publish reviews and rate works (films / books / songs), can comment on other people's reviews and rate them; can edit and delete their reviews and comments.

- Moderator - the same rights as an Authenticated User plus the right to delete and edit any reviews and comments.

- Administrator (admin) - full rights to manage the project and all its contents. Can create and delete works, categories and genres. Can assign roles to users.

- Django Administrator - Same rights as the Administrator role.

### Cloning a repository and switching to it on the command line:
```sh
https://github.com/IskanderRRR/api_yamdb.git
```
### Env file template
- We indicate that we are working with postgresql
```sh
DB_ENGINE=django.db.backends.postgresql
```
- database name
```sh
DB_NAME=postgres
```
- Login to connect to the database
```sh
POSTGRES_USER=postgres
```
- Password to connect to the database
```sh
POSTGRES_PASSWORD=postgres
```
- Service (container) name
```sh
DB_HOST=db
```
- Port for connecting to the database
```sh
DB_PORT=5432
```
### How to start a project
- Clone the repository and change into it on the command line:
```
git clone https://github.com/IgorGrrr/infra_sp2.git
```
```
cd api_yamdb
```
- Go to infra folder and run docker-compose.yaml
```
cd infra
```
```
docker-compose up
```
```
docker-compose up -d --build
```
- In the web container, perform migrations, create a superuser, and collect statics using the following commands
```
docker-compose exec web python manage.py createsuperuser
```
```
docker-compose exec web python manage.py createsuperuser
```
```
docker-compose exec web python manage.py collectstatic --no-input
```
The project is up and running at:  [localhost](http://localhost)

### Developers:
- [Iskander Ryskulov](https://github.com/IskanderRRR)
- [Pavel Homov](https://github.com/PavelHomov)
- [Georgy Popov](https://github.com/Georrgeee)