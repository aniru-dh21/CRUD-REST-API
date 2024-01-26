# CRUD REST API with NestJS, Docker, Swagger, and Prisma

Crafting a RESTful API with NestJS, Docker, Swagger, and Prisma by creating a delightful recipe management system to implement CRUD (Create, Read, Update, Delete) operations for managing recipes.

## Technologies

To build this application, I will be leveraging the power of the following tools:
- [NestJS](https://nestjs.com/): A progressive Node.js framework for building efficient, reliable, and scalable server-side applications.
- [Prisma](https://www.prisma.io/): An open-source database toolkit that makes it easy to reason about your data and how you interact with it.
- [PostgreSQL](https://www.postgresql.org/): A powerful, open source object-relational database system.
- [Docker](https://www.docker.com/): An open platform for developing, shipping, and running applications. Docker enables you to separate your applications from your infrastructure so you can deliver software quickly.
- [Swagger](https://swagger.io/): A tool for designing, building, and documenting RESTful APIs.
- [TypeScript](https://www.typescriptlang.org/): A statically typed superset of JavaScript that adds optional types, classes, and modules to the language.

Each of these technologies plays a crucial role in creating a robust, scalable, and maintainable application.

## Development Environment

- [Node.js](https://nodejs.org/en/download/) - Runtime Environment
- [Docker](https://www.docker.com/get-started/) - For containerizing database
- [Visual Studio Code](https://code.visualstudio.com/Download) - Code Editor
- [PostgreSQL](https://www.postgresql.org/download/) - Database
- [NestJS](https://docs.nestjs.com/) - Node.js Framework

## What is NestJS?

NestJS is a progressive Node.js framework that comes with a plethora of advantages, including a powerful Command Line Interface (CLI). This CLI simplifies the process of creating a new NestJS application, making it easy to start a new project anytime, anywhere.

One of the key benefits of NestJS is its rich set of built-in functionalities that significantly streamline the development process, making your life as a developer much easier.

## Docker Configuration of the Project
To store our recipes REST API, we'll use a PostgreSQL database. Docker will help us containerize this database ensuring a smooth setup and execution, regardless of the environment.

The configuration of the project(`docker-compose.yml`):
```yml
version: '3.8'
services:
  postgres:
    image: postgres:13.5
    restart: always
    environment:
      - POSTGRES_USER=recipe
      - POSTGRES_PASSWORD=RecipePassword
    volumes:
      - postgres:/var/lib/postgresql/data
    ports:
      - '5444:5432'
volumes:
  postgres:
```

Here's a quick breakdown of this configuration:
- `image: postgres:13.5`: Specifies the Docker image for the PostgreSQL database.
- `restart: always`: Ensures the container restarts if it stops.
- `environment`: Sets the username and password for the database.
- `volumes`: Mounts a volume to persist database data, even if the container is stopped or removed.
- `ports`: Exposes port `5432` on both the host machine and the container for database access.

## What is Prisma?
Prisma is an open-source database toolkit that makes it easy to reason about your data and how you interact with it.

Prisma is a powerful tool that offers a wide range of features, including:
- **Database Migrations**: Prisma makes it easy to evolve your database schema over time, without losing any data.
- **Database Seeding**: Prisma allows you to seed your database with test data.
- **Database Access**: Prisma provides a powerful API for accessing your database.
- **Database Schema Management**: Prisma allows you to define your database schema using the Prisma Schema Language.
- **Database Querying**: Prisma provides a powerful API for querying your database.
- **Database Relationships**: Prisma allows you to define relationships between your database tables.
