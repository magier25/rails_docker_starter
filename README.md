Docker development config for Rails project (with changes) from [Ruby On Whales](https://evilmartians.com/chronicles/ruby-on-whales-docker-for-ruby-rails-development).
Contains some containers:
* rails app
* postgres
* sidekiq
* redis
* webpacker
* runner

**Before usage** change app image name in `docker-compose.yml`

Run the following commands to prepare your Docker development env::

```
$ docker-compose build
$ docker-compose run runner yarn install
$ docker-compose run runner ./bin/setup
```

It builds the Docker image, installs Ruby and NodeJS dependencies, creates database, run migrations and seeds.