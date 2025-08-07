# gitea
Local Gitea instanace with Postgres and Traefik. SSH enabled.

## usage:

> [!NOTE]
> This stack is meant to be used with traefik, create the traefik network before deploying this stack: `docker network create -d bridge traefik`

Clone this repository to your local machine, edit the config file to match your environment.

```bash
git clone https://github.com/kris-smarthome/docker-gitea
cd docker-gitea
```

Create a git user, make a note of the UID and GID:

```bash
sudo adduser git
```

Add the UID and GID from the git user and the HTTPS hostname to the ```.env``` file and bring up the stack.

```bash
docker compose up -d
```

### SSH shim
To enable SSH access, an SSH shim must be used. Follow the guide here: https://docs.gitea.com/installation/install-with-docker#ssh-container-passthrough