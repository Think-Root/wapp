# What's up?

This repository is part of the [chappie_bot](https://github.com/Think-Root/chappie_bot) repository. For **chappie_bot** to work correctly, this app must also be running if you are willing to risk losing your WhatsApp account. If not, simply remove the **SendMessageToWhatsApp** function call from **chappie_bot** and forget this repository.

Wapp is essentially a wrapper around [Baileys](https://github.com/WhiskeySockets/Baileys/) that serves as an API server providing endpoints for WhatsApp automation.

## How to run

### Requirements

- [docker](https://docs.docker.com/engine/install/) or/and [docker-compose](https://docs.docker.com/compose/install/)

### Clone repo

```shell
git clone https://github.com/Think-Root/wapp.git
```

### Config

Create a **.env** file in the app root directory

```properties
AUTH_TOKEN=<your bearer token>
PORT=<server port, 3000 if leave empty>
```

### Deploy

- build `docker build -t wapp:latest -f Dockerfile .`
- run `docker run --name wapp --restart always --env-file .env -e TZ=Europe/Kiev --network think-root-network wapp:latest`
- or via docker compose `docker compose up -d`
