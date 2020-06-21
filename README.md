# docker php development environment

自分用php(Laravel)の開発環境

- php
  - composer
  - xdebug
- apache
- mysql

## 開発環境

- wsl 2
- Docker Desktop for Mac and Windows
- vscode Remote-Containers (Docker)

## usage

```sh
# create laravel project
$ docker-compose exec php bash
$ composer create-project --prefer-dist laravel/laravel app

# remove self
$ docker-compose exec php composer prune
## or run in php container
$ composer prune
```

## 動作確認

`http://localhost:8000`を確認します

## xdebug

xdebug.remote_hostに罠がありまして、`php`を指定します。

```sh
xdebug.remote_host = "php"
```

## e2e test

- standalone-chrome-debug https://github.com/SeleniumHQ/docker-selenium
- vnc vnc://localhost:5900

## todo

- [x] docker e2e test
- [ ] nginx