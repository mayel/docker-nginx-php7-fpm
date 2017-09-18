# docker-nginx-php7-fpm

Dockerfile for nginx and php-fpm together.

Composer is also installed for convenience.

Default doc root is in `/home/app/web` (this can be overridden by changing the env NGINX_ROOT in the Dockerfile) so mounting files (or mounting this repo root dir as `/home/app`) there will get them served:

  docker run -p 8080:80 --mount type=bind,source="$(pwd)",target=/home/app test


An `ERRORS` env can be set to toggle error reporting. `ERRORS=1` will trigger error reporting, everything else keeps it turned off.

Besides the Dockerfile, check out `cmd.sh` to see what happens.
