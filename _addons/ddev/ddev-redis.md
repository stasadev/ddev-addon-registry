---
title: ddev/ddev-redis
description: Redis service for DDEV
stars: 24
categories:
  - official
---

[![tests](https://github.com/ddev/ddev-redis/actions/workflows/tests.yml/badge.svg)](https://github.com/ddev/ddev-redis/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2024.svg)

## What is this?

This repository allows you to quickly install Redis into a [DDEV](https://ddev.readthedocs.io) project using the instructions below.

## Installation

For DDEV v1.23.5 or above run

```sh
ddev add-on get ddev/ddev-redis
```

For earlier versions of DDEV run

```sh
ddev get ddev/ddev-redis
```

Then restart your project

```sh
ddev restart
```

With DDEV v1.23.5+ you can choose a different Redis tag, the command below creates a `.ddev/.env.redis` file that you can commit:

1. `ddev dotenv set .ddev/.env.redis --redis-tag 7`
2. `ddev restart`

## Explanation

This Redis recipe for [DDEV](https://ddev.readthedocs.io) installs a [`.ddev/docker-compose.redis.yaml`](docker-compose.redis.yaml) using the `redis` Docker image.

Persistence is disabled by default (see [redis.conf](./redis/redis.conf)), follow the config instructions to enable it, or switch to https://github.com/ddev/ddev-redis-7 where it is enabled by default.

## Interacting with Redis

* The Redis instance will listen on TCP port 6379 (the Redis default).
* Configure your application to access Redis on the host:port `redis:6379`.
* To reach the Redis CLI interface, run `ddev redis-cli` to begin a session. You can also run Redis CLI commands directly on the command-line, e.g., `ddev redis-cli INFO`.

**Contributed and maintained by [@hussainweb](https://github.com/hussainweb) based on the original [ddev-contrib recipe](https://github.com/ddev/ddev-contrib/tree/master/docker-compose-services/redis) by [@gormus](https://github.com/gormus)**

**Co-maintained by [@stasadev](https://github.com/stasadev)**
