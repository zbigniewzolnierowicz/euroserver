# Zed's Euroserver

## Configuration

Create an .env file with the following:

```bash
# Remember to change this to your hostname
SERVER_ADDRESS=
# Password that Nextcloud uses to communicate with MariaDB
MYSQL_PASSWORD=
# Password for MariaDB maintenance
MYSQL_ROOT_PASSWORD=
# Your email address for Let's Encrypt
TRAEFIK_CERTIFICATESRESOLVERS_LE_ACME_EMAIL=
# Your timezone
TZ=
# The UID and GID of the *dedicated* account for data
PUID=
PGID=
# Path to files for Sonarr, Radarr, etc.
FILE_PATH=
# Path to Minecraft files
MINECRAFT_PATH=
# Comma-separated Minecraft server operator IGNs
OPS=
```

Change ZNC data by going to `localhost:6697`.

## Nextcloud

### Initialization

Before running `docker-compose up`, run `docker-compose up nextcloud_db` first, wait for `mysqld: ready for connections`, then `docker-compose down`, then and only then should you run `docker-compose up`.