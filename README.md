
# Setting Up a Laravel Development Environment with Docker and Docker Compose - Traefik

We forked the stack from git repository at here: [Murilolivorato Laravel Docker Environment](https://github.com/murilolivorato/laravel_docker_enviroment)

## Instructions
Laravel, the PHP web application framework, and Docker, the containerization platform, are a match made in heaven for developers seeking scalability, efficiency, and ease of deployment. In this extensive guide, we’ll delve deep into the integration of Laravel with Docker, exploring the intricacies of setting up a robust environment and establishing seamless communication between two Laravel projects.

Here’s a list of the services we’ll be creating in our Docker environment —

```
    PHP — 8.2-fpm-alpine
    Nginx — nginx:stable-alpine
    MySQL — mysql:8.0.1
    Mailhog
    PhpMyAdmin
    Redis
```

## Run those commands

Run Treafik proxy before:
- cd to treafik sub-folder.
- then run command:
``docker-compose up -d``

### Step1:
- Docker Build Image: ``docker-compose build``
### Step 2:
- Run Docker Containers: ``docker-compose up -d``
### Step 3: 
- Composer Install: ``docker-compose run --rm composer install``

Or We alsow can create Laravel Project and Set Database with command bellow:
``docker-compose run --rm composer create-project laravel/laravel``
### Step 4:
- Generate Key: ``docker-compose run --rm artisan key:generate``
### Step 5:
- Clear Config Cache: ``docker-compose run --rm artisan config:cache``
### Step 6:
- Migrate Database: ``docker-compose run  --rm artisan migrate``

