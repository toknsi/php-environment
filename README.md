# docker php development environment

自分用php(Laravel)の開発環境

- php
  - composer
  - xdebug
- apache
- mysql

## local environment

- wsl 2
- Docker Desktop for Mac and Windows
- vscode Remote-Containers (Docker)

## create laravel project

```sh
$ docker-compose exec php bash
$ composer create-project --prefer-dist laravel/laravel app
```

## 動作確認

`http://localhost:8000`を確認します

## xdebug

xdebug.remote_hostに罠がありまして、`php`を指定します。

```sh
xdebug.remote_host = "php"
```

## todo

- docker e2e test
- nginx
