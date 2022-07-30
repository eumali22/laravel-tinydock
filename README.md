# Tiny Docker Setup for Laravel 9 (PHP8 + Nginx)

## Description

laravel-tinydock is a small Laravel development setup/template utilizing Docker. It contains the initial files of a laravel project (with Breeze already installed.)

Laravel 9 already provides a development docker setup called Sail, but I wanted to use a container that is close to the setup that I will have once deployed to production. I also wanted to remove unused modules to reduce the size of the containers.

## Pre-requisites

Before using laravel-tinydock, make sure these are installed:
* Docker
* PHP
* npm
* git

## Installation

### GitHub Checkout
Clone the repository and go to your new project's root directory:

    $ git clone https://github.com/eumali22/laravel-tinydock.git <your-project-name>
    $ cd <your-project-name>

### Run the containers
Within the project root:

    $ docker-compose up

The Laravel app can be accessed in this URL: http://localhost:8080

The root directory is mounted as a volume in the docker-compose.yml, so you can edit your development files and immediately see the changes.


