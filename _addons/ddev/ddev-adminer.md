---
title: ddev/ddev-adminer
github_url: https://github.com/ddev/ddev-adminer
description: "AdminerEvo web-based database browser for DDEV"
user: ddev
repo: ddev-adminer
repo_id: 468763817
ddev_version_constraint: ""
dependencies: []
type: official
created_at: 2022-03-11
updated_at: 2025-02-13
stars: 8
---

[![tests](https://github.com/ddev/ddev-adminer/actions/workflows/tests.yml/badge.svg)](https://github.com/ddev/ddev-adminer/actions/workflows/tests.yml) ![project is maintained](https://img.shields.io/maintenance/yes/2024.svg)

# DDEV Adminer Service

## What is this?

This repository allows you to quickly install the [AdminerEvo](https://docs.adminerevo.org/) fork of the [adminer](https://www.adminer.org/) database manager into a [DDEV](https://ddev.readthedocs.io) project using just `ddev add-on get ddev/ddev-adminer`.

Adminer is a full-featured database management tool written in PHP. This service
currently ships the [official adminer container](https://hub.docker.com/_/adminer)
with no _external_ plugins. It contains all official plugins and themes and allows
to easily chose one by editing the `docker-compose.adminer.yaml` file after
installation.

AdminerEvo works with MySQL, MariaDB, PostgreSQL, SQLite, MS SQL, Oracle, Elasticsearch and MongoDB.

## Installation

For DDEV v1.23.5 or above run

```sh
ddev add-on get ddev/ddev-adminer
```

For earlier versions of DDEV run

```sh
ddev get ddev/ddev-adminer
```

Afterward run `ddev restart`

Then you can just `ddev adminer` or use `ddev describe` to get the URL (`https://<project>.ddev.site:9101`).

## What does this add-on do?

* Adds the adminer container as a service

**Contributed by [@bserem](https://github.com/bserem).**
**Maintained by DDEV team.**
