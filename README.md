# Ollama Docker

This repository provides a Dockerized setup for running [Ollama](https://ollama.com/), an open-source platform for large language models.

## Features

- Easy deployment of Ollama using Docker
- Pre-configured environment for quick setup
- Customizable via environment variables

## Getting Started

## Running Environment
The conatiner is started through terminal from Windows to utilize Docker Desktop improvements.
    I was advised not to start this from directly from WSL
My n8n server is running on the same subnet, so I added the DNS entry for ollama to make the node setup easier.
I used a bind mount to keep the model data off of C:

### Usage

```bash
git clone https://github.com/kyzersose/ollama-docker.git
cd ollama-docker
docker compose up -d
```

The Ollama service will be available at `http://localhost:11434`.

## Configuration

Edit the `docker-compose.yml` file to customize ports, volumes, or environment variables as needed.

## Contributing

Contributions are welcome! Please open issues or pull requests for improvements.

## License

This project is licensed under the MIT License.

## Ollama helpers
https://ollama.com/
To pull a new model down:
    docker exec -it [containername] ollama pull [model]
    you can also run exec commands from Docker Desktop: ollama pull [model]