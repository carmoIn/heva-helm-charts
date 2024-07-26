# Hive Mestastore

> Inspired by https://github.com/Gradiant/bigdata-charts and https://github.com/ssl-hep/hive-metastore/tree/main

:warning: This chart is currently under development. Must features have not been tested yet.

## Getting started

TODO

```
helm install hive-metastore TODO
```

## Configuration
> See [values.yaml](./values.yaml) for full list of options

### Docker image
This chart has been tested with hive 3.1.3 using https://github.com/ssl-hep/hive-metastore/ image.

### Database
The default behavior of this chart is to create a specific database for Hive Metastore, but it is possible to use an existing database:

```yaml
postgresql:
    enabled: false

connections:
  database:
    username: hive
    password: some-password
    database: metastore
    host: my-custom.database
    port: 5432
```

:warning: Please note that currently only postgresql database is accepted and the database should have the following configuration:
```
password_encryption=md5
```
