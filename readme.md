# Ansible Role: NGINX in Docker deployment
This role deploys a NGINX reverse proxy and optional letsencrypt in a Docker container.

## Variables

Defaults for variables are listed in ```defaults/main.yml```.

### Example setups
```
nginx_https_method: "nohttp"
nginx_published_ports:
  - "443:443"
```
This setup will only spawn an NGINX and only expose port 443. http traffic wont be served this way.
Letsencrypt is disabled, so you would have to provide certificates in a different way.

```
nginx_https_method: "nohttp"
nginx_published_ports:
  - "443:443"
letsencrypt: "true"
letsencrypt_default_email: "user@mail.tld"
```
Same setup as above but with Letsencrypt enabled. 

```
nginx_published_ports:
  - "127.0.0.1:80:80"
```
This way NGINX only serves on localhost. You could do this with any interface, just like in docker-compose.
