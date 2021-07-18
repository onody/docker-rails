# How to start Rails app

Create rails app. If you'd like to change app name, please replace "myapp".

```
$ docker-compose run web rails new . --force --no-deps --database=postgresql --skip-bundle
```

Build with generated Gemfile.

```
$ docker-compose build
```

Install following packages. don't forget to update "config/database.yml" => https://qiita.com/chisaki0606/items/a4b42af5c4735c94057a

```
$ docker-compose run web rails webpacker:install
$ docker-compose run web rake db:create
```

Start rails application.

```
$ docker-compose up
```
