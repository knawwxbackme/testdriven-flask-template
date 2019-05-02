# Test Driven Server

## Prerequisites

- Python 3.7
- Docker (latest)

## Quick Start

Clone repo, then run:
```
docker-compose -f docker-compose-dev.yml up -d --build 
docker-compose -f docker-compose-dev.yml exec users python manage.py recreate-db
docker-compose -f docker-compose-dev.yml exec users python manage.py seed-db 
```
To run tests
```
docker-compose -f docker-compose-dev.yml exec users python manage.py test
```
## Switching Environment
```
eval $(docker-machine env [DOCKER_MACHINE_NAME])
```
