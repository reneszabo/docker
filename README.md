# Home Docker Lab

## Environment Variables 

Rename file from .env.template to .env

```dotenv
PATH_MEDIA_FILEBOT=/path/to/folder
PATH_MEDIA_TORRENT=/path/to/folder
PATH_MEDIA_PLEX=/path/to/folder
SAMBA_USER=username
SAMBA_PASSWORD=password
TRANSMISSION_USER=username
TRANSMISSION_PASSWORD=password
PIHOLE_PASSWORD=password
PUID=1003
PGID=1006
TZ=TimeZone
SERVER_NAME=server-name
CADDY_MERCURE_JWT_SECRET='secret!'
```

## Caddy

Rename file from Caddyfile.template to Caddyfile and add Domain for each folder you need. Remember to map volumes for the code or proxy to other services.

## Pihole

Not configured for DHCP. No other configuration is needed. I am not exposing port 80 since it is proxied by Caddy

## Plex

No configuration, other than environmental variable that maps path to media files.

## samba

Use environmental Variable to configure path to files.

## transmission

Use environmental variables to configure username and passowrd for network drive.
If more drives want to be added, it needs to be added in docker compose command, add new env variable with the pass and map the new volume.
