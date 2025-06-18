# banking-app-golang

This project is a modern, scalable banking application built with Golang as the core programming language. It leverages a cloud-native architecture to handle financial transactions and data management efficiently. The application uses PostgreSQL for secure and reliable data storage, while SQLC is used to generate Go code from SQL queries, ensuring type-safety and clean interaction with the database.

The application is containerized with Docker for portability and ease of deployment, and orchestrated using Kubernetesfor seamless scaling and management in the cloud. Hosted on AWS, the app utilizes cloud services to ensure high availability, disaster recovery, and security.

Designed using microservices architecture, each service is independently deployable, scalable, and fault-tolerant, making the system both resilient and efficient in a production environment.

Key Technologies:

Golang: Main backend language for high-performance, concurrent processing.

PostgreSQL: Reliable relational database management system for transactional data.

SQLC: Automatically generates Go code from SQL queries, providing type-safe database interactions.

Docker: Containerization for creating portable, isolated environments for microservices.

Kubernetes: Orchestration for automating deployment, scaling, and management of containerized services.

AWS: Cloud infrastructure for hosting the app and leveraging various AWS services like EC2, RDS, S3, etc.

## Setup local development

### Install tools

- [Docker desktop](https://www.docker.com/products/docker-desktop)
- [TablePlus](https://tableplus.com/)
- [Golang](https://golang.org/)
- [Homebrew](https://brew.sh/)
- [Migrate](https://github.com/golang-migrate/migrate/tree/master/cmd/migrate)

  ```bash
  brew install golang-migrate
  ```

- [Sqlc](https://github.com/kyleconroy/sqlc#installation)

  ```bash
  brew install sqlc
  ```

### Setup infrastructure

- Start postgres container:

  ```bash
  make postgres
  ```

- Create simple_bank database:

  ```bash
  make createdb
  ```

- Run db migration up all versions:

  ```bash
  make migrateup
  ```

- Run db migration down all versions:

  ```bash
  make migratedown
  ```

### How to generate code

- Generate SQL CRUD with sqlc:

  ```bash
  make sqlc
  ```
  