# Katalon example Employees MySQL database - Docker Compose

## Description

This is a docker-compose file to be use as a sample MySQL server for Katalon example Employees MySQL database project <https://github.com/indraginanjar/katalon-example-employees-mysql-database>.

`employees` database served by the MySQL server is retrieved from datacharmer / test_db's github  <https://github.com/datacharmer/test_db>.

## About this documentation

### Asumptions

- User has a mysql client application installed in his/her machine

## How to run

1. Pull sample database files

    ```bash
    git submodule update
    ```

2. Disable calling other sql/dump files from employees.sql, because it will be failed.

    ```bash
    ./scripts/test_db_employees_disable_call_dump.sh
    ```

3. To start MySQL Service, run:

    ```bash
    docker-compose up --force-recreate
    ```

## How to stop

To shutdown, the services

```bash
docker-compose down -v
```

## Accessing MySQL

To be able access the MySQL server type:

Syntax:

```bash
mysql -u root -p
```
