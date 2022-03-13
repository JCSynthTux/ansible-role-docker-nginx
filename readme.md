# Ansible Role: NGINX in Docker deployment
This role deploys a NGINX reverse proxy and optional letsencrypt in a Docker container.

## Variables

There are a few variables to set:

```nginx_network: "nginx_network"``` required - name of the nginx network

```letsencrypt_install: true``` optional - true to install letsencrypt - false to uninstall or not setup

```letsencrypt_mail: "your.mail@provider.tld"``` required - for letsencrypt
