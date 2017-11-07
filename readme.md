# Auto Caddy
Restarts Caddy in case **Cadyfile** in **mnt/** directory changes.

## Getting started
1. clone this repo
2. create custom **Cadyfile** in **mnt/** directory
3. `docker-compose up -d` in clone directory

## Volumes
*relative to clone directory*
* **mnt/** contains **Caddyfile** and **caddy.log**
* **certs/** contain ssl certificates

## Networks
* Host network