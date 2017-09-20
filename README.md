# Docker Grav

Docker setup to run grav in docker.

## Setup Grav

Place grav under docroot folder. You can do it by running `composer create-project getgrav/grav ./docroot` or you can download it manually and place it there. (It's important to keep ./docroot as the path because this is the path that will be mounted in the containers).

Set right permissions:

```
chmod o+w docroot/user/config
chmod o+w -R docroot/cache
chmod o+w -R docroot/logs
chmod o+w -R docroot/images
chmod o+w -R docroot/assets
chmod o+w -R docroot/user/data
chmod o+w -R docroot/backup
chmod o+w -R docroot/tmp
chmod o+w -R docroot/user/accounts
```

## Build Environment

To build this environment you need recent docker composer and docker versions.
After placing grav in the right folder, you should run `docker-compose up -d` and voilá! You can access your Grav installation at `http://localhost:8080`

Have fun!
