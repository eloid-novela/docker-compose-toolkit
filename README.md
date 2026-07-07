# Docker Compose Toolkit

A collection of `make` commands designed to simplify the management of projects that use Docker Compose.

## About

This project brings together the most common Docker Compose commands into a single `Makefile`, making development workflows faster, simpler, and more consistent.

Instead of running long commands like:

```bash
docker compose up -d
docker compose down
docker compose logs -f
docker compose exec app bash
```

You can simply run:

```bash
make up
make down
make logs
make bash
```

## Prerequisites

* Docker
* Docker Compose
* GNU Make

Verify that everything is installed:

```bash
docker --version
docker compose version
make --version
```

## Installation

Clone the repository:

```bash
git clone https://github.com/eloid-novela/docker-compose-toolkit.git
cd docker-compose-toolkit
```

Copy the `Makefile` into your project directory or customize it as needed.

## Usage

Run commands from your terminal:

```bash
make <command>
```

Examples:

```bash
make up
make down
make restart
make build
make logs
```

## Available Commands

| Command        | Description                                      |
| -------------- | ------------------------------------------------ |
| `make up`      | Start containers in detached mode                |
| `make down`    | Stop and remove containers                       |
| `make build`   | Build or rebuild images                          |
| `make restart` | Restart containers                               |
| `make stop`    | Stop running containers                          |
| `make start`   | Start existing containers                        |
| `make logs`    | Follow container logs in real time               |
| `make ps`      | List running containers                          |
| `make bash`    | Open a Bash shell inside a container             |
| `make sh`      | Open a SH shell inside a container               |
| `make exec`    | Execute a command inside a service               |
| `make clean`   | Remove containers, volumes, and unused resources |

> **Note:** Some commands depend on your `Makefile` configuration and the service names defined in your `docker-compose.yml` or `compose.yaml` file.

## Customization

You can customize the `Makefile` to fit your project by changing variables such as:

* Main service name
* Compose file name
* Docker Compose flags
* Environment (`development`, `production`, etc.)

## Contributing

Contributions are welcome!

If you have suggestions for improvements or new commands, feel free to open an **Issue** or submit a **Pull Request**.

## License

This project is licensed under the MIT License.
