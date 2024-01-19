# Projeto de Interação de Serviços com RabbitMQ

Este é um projeto pequeno que utiliza microserviços para interação entre serviços, implementado em JavaScript (Node.js) e Java (Spring Boot). O banco de dados utilizado é o PostgreSQL para um dos serviços e o MongoDB para outro.

## Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas em sua máquina:

- [Node.js](https://nodejs.org/) (v14.x ou superior)
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-downloads.html) (v11 ou superior)
- [PostgreSQL](https://www.postgresql.org/download/)
- [MongoDB](https://www.mongodb.com/try/download/community)
- [RabbitMQ](https://www.rabbitmq.com/download.html)
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)

## Configuração do Ambiente

1. **Configuração do PostgreSQL¹:**
   - Crie um banco de dados chamado `auth-db`.
   - Atualize as informações de conexão no arquivo `postgres-service/src/main/resources/application.properties`.

   **Configuração do PostgreSQL²:**
   - Crie um banco de dados chamado `product-db`.
   - Atualize as informações de conexão no arquivo `postgres-service/src/main/resources/application.properties`.

2. **Configuração do MongoDB:**
   - Inicie o servidor MongoDB.
   - O serviço utilizará um banco de dados chamado `sales-db`.

3. **Configuração do RabbitMQ:**
   - Certifique-se de que o RabbitMQ está em execução.
   - Não são necessárias configurações adicionais, pois o projeto usa as configurações padrão.


- **postgres-service:**
  - Responsável por operações relacionadas ao PostgreSQL.
  - Utiliza Node.js (JavaScript).
  - Se conecta ao banco de dados PostgreSQL.

- **mongo-service:**
  - Responsável por operações relacionadas ao MongoDB.
  - Utiliza Java (Spring Boot).
  - Se conecta ao banco de dados MongoDB.

## Docker e Docker Compose

O projeto utiliza Docker
