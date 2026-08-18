# Quiz Game Platform

Plataforma interativa para criação e realização de quizzes de múltipla escolha, desenvolvida pela equipa **Build & Learn IT**.

## Objetivo

O **Quiz Game Platform** permite que utilizadores criem, editem e joguem quizzes de múltipla escolha.

A plataforma deverá incluir funcionalidades como:

* Registo e login de utilizadores
* Criação e gestão de quizzes
* Perguntas com múltiplas opções
* Gameplay interativo
* Temporizador
* Sistema de pontuação
* Resultados finais
* Leaderboard
* Modo equipa
* Histórico de partidas

## Tech Stack

### Backend

* Java 21
* Spring Boot
* Spring Web
* Spring Data JPA
* Hibernate
* Spring Security
* JWT
* Maven

### Frontend

* HTML5
* CSS3
* JavaScript ES6+

### Database

* PostgreSQL

### Testing

* JUnit
* Spring Boot Test
* Postman

### Version Control

* Git
* GitHub

## Estrutura Geral do Projeto

```text
quiz-game-platform/
│
├── backend/
│   ├── pom.xml
│   └── src/
│       ├── main/
│       │   ├── java/
│       │   │   └── com/
│       │   │       └── buildlearn/
│       │   │           └── quizgame/
│       │   │               ├── config/
│       │   │               ├── controller/
│       │   │               ├── dto/
│       │   │               ├── exception/
│       │   │               ├── model/
│       │   │               ├── repository/
│       │   │               ├── security/
│       │   │               ├── service/
│       │   │               └── QuizGameApplication.java
│       │   │
│       │   └── resources/
│       │       └── application.properties
│       │
│       └── test/
│
├── frontend/
│   ├── index.html
│   ├── pages/
│   ├── css/
│   ├── js/
│   │   ├── api/
│   │   ├── auth/
│   │   ├── quiz/
│   │   ├── game/
│   │   └── utils/
│   └── assets/
│
├── docs/
│   ├── architecture.md
│   └── .env.example
│
├── .gitignore
└── README.md
```

## Arquitetura

A aplicação segue uma arquitetura cliente-servidor.

```text
Frontend
   ↓
HTTP / JSON
   ↓
Spring Boot REST API
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
PostgreSQL
```

O frontend comunica com o backend através de uma API REST.

O backend é responsável pela lógica de negócio, autenticação, validação, acesso à base de dados e processamento das partidas.

## Como executar o Backend

### Pré-requisitos

É necessário ter instalado:

* Java 21
* Maven
* PostgreSQL

### Executar

Entrar na pasta:

```bash
cd backend
```

Instalar as dependências e compilar:

```bash
mvn clean install
```

Executar a aplicação:

```bash
mvn spring-boot:run
```

Por padrão, a API deverá ficar disponível em:

```text
http://localhost:8080
```

## Configuração da Base de Dados

Criar uma base de dados PostgreSQL para o projeto.

As configurações locais deverão ser definidas através das variáveis de ambiente ou do ficheiro de configuração local.

Exemplo:

```env
DATABASE_URL=
DATABASE_USERNAME=
DATABASE_PASSWORD=
JWT_SECRET=
```

Nunca devem ser adicionadas passwords, tokens ou outras credenciais reais ao repositório.

## Como executar o Frontend

Entrar na pasta:

```bash
cd frontend
```

Para desenvolvimento local, o frontend pode ser aberto através de um servidor local.

Por exemplo, utilizando a extensão **Live Server** no VS Code.

O frontend deverá comunicar com a API disponível em:

```text
http://localhost:8080/api
```

## Git Workflow

O projeto utiliza as seguintes branches principais:

```text
main
develop
feature/*
fix/*
```

### `main`

Contém apenas versões estáveis do projeto.

Não devem ser feitos pushes diretos para esta branch.

### `develop`

Branch utilizada para integração do trabalho da equipa.

As funcionalidades concluídas devem ser integradas nesta branch através de Pull Requests.

### `feature/*`

Cada nova funcionalidade deverá ser desenvolvida numa branch própria criada a partir da `develop`.

Exemplos:

```text
feature/backend-setup
feature/database-setup
feature/frontend-setup
feature/auth
feature/quiz-crud
feature/gameplay
```

### `fix/*`

Utilizada para correções de bugs.

Exemplo:

```text
fix/login-validation
```

## Fluxo de Desenvolvimento

```text
develop
   ↓
feature/nome-da-feature
   ↓
desenvolvimento
   ↓
Pull Request
   ↓
Code Review
   ↓
develop
   ↓
testes e integração
   ↓
Pull Request
   ↓
main
```

## Convenção de Commits

Utilizamos mensagens de commit claras e objetivas.

Exemplos:

```text
feat: add user registration
feat: create quiz endpoint
fix: correct login validation
docs: update project documentation
test: add authentication tests
refactor: reorganize quiz service
chore: configure project
```

## Equipa

### Khayllane Nyambir
### Cesarino Nhabangue
### Mirafilda Gamboa
### Lonel Vasco
### Manuel Guirute


## Gestão de Tarefas

As tarefas são organizadas através de **GitHub Issues** e do **GitHub Project Board**.

Estados utilizados:

```text
Todo
In Progress
Review
Done
```

## Definition of Done

Uma tarefa só deve ser considerada concluída quando:

* O código estiver funcional
* A tarefa tiver sido testada localmente
* Não existirem erros críticos conhecidos
* O Pull Request tiver sido criado
* O código tiver sido revisto
* O trabalho tiver sido integrado na `develop`
* A documentação relevante tiver sido atualizada

## Prazo

Prazo total do projeto:

**2 semanas**

## Organização

Projeto desenvolvido no âmbito da iniciativa **Build & Learn IT**.
