# docker-nginx-php7-fpm

Dockerfile for nginx and php-fpm together.

Composer is also installed for convenience.

Default doc root is in `/usr/share/nginx/html` so mounting files there will get them served. This can be overridden by changing the env NGINX_ROOT in the container.

An `ERRORS` env can be set to toggle error reporting. `ERRORS=1` will trigger error reporting, everything else keeps it turned off.

Besides the Dockerfile, check out `cmd.sh` to see what happens.
