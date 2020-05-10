# Zed's Euroserver

## Configuration

Create an .env file with the following:

```bash
# Your hostname
SERVER_ADDRESS=
# The password Nextcloud will use to connect to MariaDB
MYSQL_PASSWORD=
# The password for MariaDB's maintenance
MYSQL_ROOT_PASSWORD=
# Your e-mail address
TRAEFIK_CERTIFICATESRESOLVERS_LE_ACME_EMAIL=
```

Change ZNC data by going to `localhost:6697`.

## Nextcloud

### Initialization

Before running `docker-compose up`, run `docker-compose up nextcloud_db` first, wait for `mysqld: ready for connections`, then `docker-compose down`, then and only then should you run `docker-compose up`.