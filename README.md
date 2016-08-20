# Drake

Dockeriszed development environment for Ruby + mongoDB + PostgreSQL + Redis.


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
> Create alias for frequently used commands.
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
|---------------------|
|   mongoDB  |  27017 |
| PostgreSQL |  5432  |
|    Redis   |  6379  |


## Database Credentials

See `Dockerfile` for corresponding database.


## Customize

Just edit the `Dockerfile` of your service!


## License

MIT
