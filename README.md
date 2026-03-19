# Minerva

Client/server training management system solution.

## Key features

- Integrate A.I. to help trough tasks.

## Project organization

This project is split in multiple projects/repositories.

- [Minerva](https://github.com/alexandrelamberty/minerva)
This repository contains all the related projects, as well as the necessary infrastructure for running this project.

- [Minerva Design Guidelines](https://github.com/alexandrelamberty/minerva-design-guidelines)
Logos, typography and color palettes guidelines.

- [Entity relationship Model (RM)](https://github.com/alexandrelamberty/minerva-erm)
Business Analysis of the basic requirement of the system.

- [Relational Modal (RM)](https://github.com/alexandrelamberty/minerva-rm)
Database structure of the system.

- [Minerva API Specification](https://github.com/alexandrelamberty/minerva-erm)
OpenAPI specification describing how to interact with the system.

- [Minerva API](https://github.com/alexandrelamberty/minerva-api)
Server application exposing an API that implement the above specification.

- [Minerva Web Application](https://github.com/alexandrelamberty/minerva-web-app)
Web application that consume the above API to interact with the system.

- [Minerva Website](https://github.com/alexandrelamberty/minerva-website)
Business website that provide a catalogue of trainings that you can enrol on.

## Project architecture

## Project technologies

Here are some of the languages, formats, frameworks, and technologies used trough this project.

- [JavaScript]()
- [TypeScript]()
- [HTML]()
- [CSS]()
- [TailwindCSS]()
- [Vite]()
- [PNPM]()
- [React]()
- [Redux]()
- [Node.js]()
- [Express.js]()
- [Sequelize]()
- [OpenAPI]()
- [OpenAI]()
- [Docker]()
- [NGINX]()

## Demo

## Requirements

- [Docker](https://docs.docker.com/get-started/overview/)
- [Docker Compose](https://docs.docker.com/compose/)

## Usage

### Docker

The stack provides three services that require environment variables in order to function properly.

Create an .env file and fill it with the following configuration:

```properties
# Minerva Environment variables
# Node
NODE_ENV=development
# Server Application
API_PORT=3000
DB_SERVER=localhost
DB_ROOT_PASSWORD=localhost
DB_DATABASE=minerva
DB_USERNAME=minerva
DB_PASSWORD=minerva
DB_PORT=3306
JWT_SECRET=d7a481461577ba4c3c4c6946cca7204b
JWT_EXPIRE=1d
JWT_ISSUER=minerva
JWT_AUDIENCE=web-minerva
MAIL_SERVER=xxx
MAIL_USERNAME=xxx
MAIL_PASSWORD=xxx
MAIL_VALIDATION=false
OPENAI_API_KEY=d7a481461577ba4c3c4c6946cca7204b
# Web Application
VITE_API_URL=http://localhost:3000
# Website
API_URL=http://localhost:3000
```

> Verify that the ports specified, `API_PORT` and `DB_PORT` are not already in use.
> Create an account on the [OpenAI](https://platform.openai.com/) platform to benefit from the integration of A.I. in the system. :rofl:

Start all the services with the provided configuration

```shell
docker compose --env-file .env up 
```

Now the system must be up and running!

You can now access the services at the following url:

- Website @ [http://localhost:80](http://localhost:80)
- Web Application @ [http://localhost:8080](http://localhost:8080)
- API @ [http://localhost:8090](http://localhost:8090)

### Portainer

Use the Minerva main repository that contains the Docker infrastructure.

```shell
https://github.com/alexandrelamberty/minerva
```

## Development

You can run any service needed for the server application or web application.

- **mysql** MySQL instance
- **web**  Admin web application
- **api** API server application

Start the specified service with the provided configuration

```shell
docker compose --env-file .env up service_name
```
