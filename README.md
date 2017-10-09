# Docker Grav

Docker setup to run grav in docker.

## Setup Grav

Place grav under docroot folder. You can do it by running `composer create-project getgrav/grav ./docroot` or you can download it manually and place it there. (It's important to keep ./docroot as the path because this is the path that will be mounted in the containers).

Set right permissions:

```
chmod o+w docroot/user/config
chmod -R o+w docroot/cache
chmod -R o+w docroot/logs
chmod -R o+w docroot/images
chmod -R o+w docroot/assets
chmod -R o+w docroot/user/data
chmod -R o+w docroot/backup
chmod -R o+w docroot/tmp
chmod -R o+w docroot/user/accounts
chmod -R o+w docroot/user/pages
```

## Build Environment

To build this environment you need recent docker composer and docker versions.
After placing grav in the right folder, you should run `docker-compose up -d` and voilá! You can access your Grav installation at `http://localhost:8080`

Have fun!
