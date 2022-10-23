# docker-traefik

## About

Universal traefik controller for all docker-compose installations. Listens for incoming requests on http or https (port 80 or 443) and distributes it to the docker container configured for a specific domain. 

Example docker container will be provided soon. 


## Configuration

The docker container must be assigned to following network, so it can be managed by traefik:

````yaml
networks:
  default:
    name: traefik-default
````


## Important

The file **acme.json** must have **600** permissions (letsencrypt requirement).
