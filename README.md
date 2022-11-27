Odoo Docker ARM
===============

Docker images to run Odoo on ARM, which are hosted on [Docker Hub](https://hub.docker.com/r/thhoangtran/odoo/tags). These images are referenced from [Odoo Docker](https://github.com/odoo/docker), which are altered to work for ARM builds.

# Supported tags
- `16`, `latest`
- `15`
- `14`
- `13` (end of LTS)
- `12` (end of LTS)
- `11` (end of LTS)

# How to use this image

Pretty much same as how you would use Odoo official images, but use `thhoangtran/odoo:tag` instead of `odoo:tag`.

```shell
docker run -d -e POSTGRES_USER=odoo -e POSTGRES_PASSWORD=odoo -e POSTGRES_DB=postgres --name db postgres:13
docker run -p 8069:8069 --name odoo --link db:db -t thhoangtran/odoo
```

Check [this document](https://github.com/docker-library/docs/tree/master/odoo) for more information.
