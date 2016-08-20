# Drake

Dockeriszed development environment for [Ruby](https://www.ruby-lang.org/) with batteries included ([Docker Compose](https://docs.docker.com/compose/), [mongoDB](https://www.mongodb.com/), [PostgreSQL](https://www.postgresql.org/) & [Redis](http://redis.io/))


## Setup

    cd your-project
    git clone https://github.com/harshjv/drake.git


## Start services

    cd drake
    docker-compose up -d


## Usage

Inside `drake` directory;

    docker-compose run workspace rake abc
    docker-compose run workspace bundle exec def


> **Pro-Tip™**
>
> Create aliases for frequently used commands.
>
>     alias drake='docker-compose run workspace rake'
>     alias dbundle='docker-compose run workspace bundle'
>
> Then use it as;
>
>     drake abc
>     dbundle def


## Database Usage

After starting services using `docker-compose`, **mongoDB**, **PostgreSQL**, and **Redis** will be running in background and will listen on following ports;


|  Database  |  Port  |
|------------|--------|
|   mongoDB  |  27017 |
| PostgreSQL |  5432  |
|    Redis   |  6379  |


## Database Credentials

See [docker-compose.yml](docker-compose.yml)


## Customize

Just edit the `Dockerfile` of your service!


## License

MIT
