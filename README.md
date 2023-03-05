# docker-traefik

## About

Universal traefik controller for all docker-compose installations. Listens for incoming requests on http or https (port 80 or 443) and distributes it to the docker container configured for a specific domain. 

## Configuration

### Environment variables
The Email address for the LetsEncyrpt certificate resolver must be set in `.env`. Copy from `.env.example` and set own email address!

```
TRAEFIK_CERTIFICATESRESOLVERS_LETSENCRYPT_ACME_EMAIL="acme@example.com"
```

### Docker Container

The docker container must be assigned to following network, so it can be managed by traefik:

````yaml
networks:
  default:
    name: traefik-default
````


## acme.json - Important

The file **acme.json** must have **600** permissions (letsencrypt requirement).
