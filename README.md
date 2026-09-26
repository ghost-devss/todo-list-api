# 📝 To-Do List API

A simple REST API for managing a to-do list, built with **Java** and **Spring Boot**.

This project was created as a practical study project to learn the fundamentals of REST APIs, HTTP methods, JSON, Spring Boot controllers, dependency injection, and Maven.

> 🚧 **Study project:** tasks are currently stored in memory, so all data is lost when the application is restarted.

## 🚀 Technologies

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=openjdk)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-4.1.1-6DB33F?style=for-the-badge&logo=springboot)
![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven)
![REST API](https://img.shields.io/badge/REST-API-005571?style=for-the-badge)

## 📌 Features

The API currently provides three operations:

- List all tasks
- Add a new task
- Clear all tasks

Tasks are stored in an in-memory `ArrayList` and are represented as strings.

## 🔌 API Endpoints

| Method | Endpoint | Description |
|:------:|----------|-------------|
| `GET` | `/tasks` | Lists all registered tasks |
| `POST` | `/tasks` | Adds a new task |
| `DELETE` | `/tasks` | Removes all registered tasks |

### 📋 Get all tasks

```http
GET http://localhost:8080/tasks
```

Example response:

```json
[
  "Study Java",
  "Learn Spring Boot",
  "Build a REST API"
]
```

### ➕ Create a task

The task is sent as plain text in the request body.

```http
POST http://localhost:8080/tasks
Content-Type: text/plain
```

```text
Study Spring Boot
```

### 🗑️ Clear all tasks

```http
DELETE http://localhost:8080/tasks
```

## 🏗️ Project Structure

```text
src
├── main
│   ├── java
│   │   └── tech.buildrun.api
│   │       ├── ApiApplication.java
│   │       └── controller
│   │           └── ApiController.java
│   │
│   └── resources
│       └── application.properties
│
└── test
    └── java
        └── tech.buildrun.api
            └── ApiApplicationTests.java
```

### `ApiApplication`

The main class responsible for starting the Spring Boot application.

### `ApiController`

Contains the API endpoints for listing, creating, and clearing tasks.

The controller also uses dependency injection to receive an `ObjectMapper`, which converts the task list into JSON.

## ⚙️ How to Run

### Prerequisites

- Java 21 or later
- Git

The project includes the **Maven Wrapper**, so Maven does not need to be installed separately.

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/todo-list-api.git
cd todo-list-api
```

### 2. Run the application

**Windows:**

```bash
mvnw.cmd spring-boot:run
```

**Linux/macOS:**

```bash
./mvnw spring-boot:run
```

The API will be available at:

```text
http://localhost:8080
```

## 🧪 Testing the API

You can test the endpoints with **HTTPie**, **Postman**, or **cURL**.

Using HTTPie:

```bash
http GET :8080/tasks
http POST :8080/tasks task="Study Java"
http DELETE :8080/tasks
```

Using cURL:

```bash
curl http://localhost:8080/tasks
```

## 📚 What I Learned

While developing this project, I practiced:

- Building a REST API with Spring Boot
- Understanding HTTP methods
- Creating endpoints with Spring annotations
- Using `@RestController`
- Using `@GetMapping`, `@PostMapping`, and `@DeleteMapping`
- Receiving request data with `@RequestBody`
- Returning responses with `ResponseEntity`
- Working with JSON
- Understanding dependency injection
- Using `ObjectMapper`
- Managing dependencies with Maven
- Using Git and GitHub for version control

## 🎯 Next Steps

- [ ] Persist tasks in a database
- [ ] Create a dedicated Task model/entity
- [ ] Update and delete individual tasks
- [ ] Add service and repository layers
- [ ] Add input validation
- [ ] Improve exception handling
- [ ] Add automated tests
- [ ] Add Swagger/OpenAPI documentation
- [ ] Add authentication
- [ ] Deploy the application

---

# 🇧🇷 Português

## 📝 API de Lista de Tarefas

Uma API REST simples para gerenciamento de uma lista de tarefas, desenvolvida com **Java** e **Spring Boot**.

Este projeto foi criado como um projeto prático de estudos para aprender os fundamentos de APIs REST, métodos HTTP, JSON, controllers do Spring Boot, injeção de dependência e Maven.

> 🚧 **Projeto de estudos:** as tarefas são armazenadas atualmente apenas em memória. Portanto, todos os dados são perdidos quando a aplicação é reiniciada.

## 🚀 Tecnologias

- ☕ Java 21
- 🌱 Spring Boot 4.1.1
- 📦 Maven
- 🌐 REST API
- 🔄 JSON
- 🧪 HTTPie

## 📌 Funcionalidades

A API possui atualmente três operações:

- Listar todas as tarefas
- Adicionar uma nova tarefa
- Limpar todas as tarefas

As tarefas são armazenadas em um `ArrayList` em memória e representadas como strings.

## 🔌 Endpoints

| Método | Endpoint | Descrição |
|:------:|----------|-----------|
| `GET` | `/tasks` | Lista todas as tarefas cadastradas |
| `POST` | `/tasks` | Adiciona uma nova tarefa |
| `DELETE` | `/tasks` | Remove todas as tarefas cadastradas |

### 📋 Listar tarefas

```http
GET http://localhost:8080/tasks
```

Exemplo de resposta:

```json
[
  "Estudar Java",
  "Aprender Spring Boot",
  "Criar uma API REST"
]
```

### ➕ Criar tarefa

A tarefa é enviada como texto no corpo da requisição.

```http
POST http://localhost:8080/tasks
Content-Type: text/plain
```

```text
Estudar Spring Boot
```

### 🗑️ Limpar tarefas

```http
DELETE http://localhost:8080/tasks
```

## 🏗️ Estrutura do projeto

```text
src
├── main
│   ├── java
│   │   └── tech.buildrun.api
│   │       ├── ApiApplication.java
│   │       └── controller
│   │           └── ApiController.java
│   │
│   └── resources
│       └── application.properties
│
└── test
    └── java
        └── tech.buildrun.api
            └── ApiApplicationTests.java
```

### `ApiApplication`

Classe principal responsável por iniciar a aplicação Spring Boot.

### `ApiController`

Contém os endpoints responsáveis por listar, criar e limpar as tarefas.

O controller também utiliza injeção de dependência para receber um `ObjectMapper`, responsável por transformar a lista de tarefas em JSON.

## ⚙️ Como executar

### Pré-requisitos

- Java 21 ou superior
- Git

O projeto possui o **Maven Wrapper**, então não é necessário instalar o Maven separadamente.

### 1. Clone o repositório

```bash
git clone https://github.com/SEU-USUARIO/todo-list-api.git
cd todo-list-api
```

### 2. Execute a aplicação

**Windows:**

```bash
mvnw.cmd spring-boot:run
```

**Linux/macOS:**

```bash
./mvnw spring-boot:run
```

A API estará disponível em:

```text
http://localhost:8080
```

## 🧪 Testando a API

Você pode testar os endpoints utilizando **HTTPie**, **Postman** ou **cURL**.

Com HTTPie:

```bash
http GET :8080/tasks
http POST :8080/tasks task="Estudar Java"
http DELETE :8080/tasks
```

Com cURL:

```bash
curl http://localhost:8080/tasks
```

## 📚 O que aprendi

Durante o desenvolvimento deste projeto, pratiquei:

- Criação de uma API REST com Spring Boot
- Entendimento dos métodos HTTP
- Criação de endpoints utilizando anotações do Spring
- Utilização de `@RestController`
- Utilização de `@GetMapping`, `@PostMapping` e `@DeleteMapping`
- Recebimento de dados através de `@RequestBody`
- Retorno de respostas utilizando `ResponseEntity`
- Manipulação de JSON
- Conceito de injeção de dependência
- Utilização do `ObjectMapper`
- Gerenciamento de dependências com Maven
- Utilização do Git e GitHub para versionamento

## 🎯 Próximos passos

- [ ] Persistir as tarefas em um banco de dados
- [ ] Criar um modelo/entidade específica para as tarefas
- [ ] Atualizar e excluir tarefas individualmente
- [ ] Adicionar camadas de service e repository
- [ ] Adicionar validação dos dados
- [ ] Melhorar o tratamento de exceções
- [ ] Adicionar testes automatizados
- [ ] Adicionar documentação com Swagger/OpenAPI
- [ ] Adicionar autenticação
- [ ] Fazer o deploy da aplicação

---

## 👩‍💻 Author

**Hellen**

This project was created as part of my studies in **Java, Spring Boot and backend development**.
