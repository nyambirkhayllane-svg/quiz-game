# Quiz Game Platform

Plataforma interativa para criação e realização de quizzes de múltipla escolha, desenvolvida pela equipa **Build & Learn IT**.

## Objetivo

O **Quiz Game Platform** tem como objetivo permitir que os utilizadores criem e joguem quizzes de múltipla escolha, individualmente ou em equipa.

Entre as funcionalidades previstas estão:

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

## Stack Proposta

> **Nota:** esta stack é uma proposta inicial e ainda deverá ser validada pela equipa.
> Como a equipa está numa fase de aprendizagem e o prazo do projeto é de 2 semanas, as tecnologias podem ser simplificadas ou ajustadas conforme o conhecimento da equipa e a complexidade encontrada durante o desenvolvimento.

### Backend

Tecnologias inicialmente consideradas:

* Java
* Spring Boot

O Java foi considerado porque é uma das tecnologias já conhecidas pela equipa.

O Spring Boot foi proposto porque facilita a criação de APIs e aplicações web em Java, mas ainda deverá ser avaliado pela equipa antes de ser considerado uma decisão definitiva.

### Frontend

Tecnologias inicialmente consideradas:

* HTML5
* CSS3
* JavaScript

HTML e CSS serão utilizados para a estrutura e apresentação da interface.

JavaScript será necessário para funcionalidades como:

* comunicação com a API;
* carregamento dinâmico de quizzes;
* envio de respostas;
* temporizador;
* atualização de pontuação;
* autenticação;
* leaderboard.

### Base de Dados

Proposta inicial:

* PostgreSQL

O PostgreSQL foi sugerido por ser uma base de dados relacional e por o projeto possuir várias entidades relacionadas, como:

* utilizadores;
* quizzes;
* perguntas;
* opções;
* partidas;
* respostas;
* resultados;
* equipas.


### Tecnologias e Ferramentas a Avaliar

As seguintes tecnologias foram sugeridas, mas **não são ainda obrigatórias**:

* Spring Web
* Spring Data JPA
* Hibernate
* Spring Security
* JWT
* Maven
* JUnit
* Spring Boot Test
* Postman

Estas ferramentas só deverão ser adotadas se forem necessárias para o projeto e se a equipa conseguir utilizá-las dentro do prazo disponível.

## Arquitetura Proposta

A arquitetura inicial considerada é:

```text
Frontend
   ↓
HTTP / JSON
   ↓
Backend / API REST
   ↓
Lógica da aplicação
   ↓
Acesso aos dados
   ↓
Base de Dados
```

Caso a equipa confirme a utilização de Spring Boot, a organização poderá seguir uma estrutura semelhante a:

```text
Frontend
   ↓
API REST
   ↓
Controller
   ↓
Service
   ↓
Repository
   ↓
PostgreSQL
```

Esta estrutura não é definitiva e poderá ser ajustada conforme a evolução do projeto.

## Estrutura Proposta do Projeto

```text
quiz-game-platform/
│
├── backend/
│
├── frontend/
│
├── docs/
│   ├── architecture.md
│   └── .env.example
│
├── .gitignore
└── README.md
```

A estrutura interna das pastas `backend` e `frontend` será definida pelos membros responsáveis por essas áreas durante a Fase 1.

## Git Workflow

O projeto utiliza as seguintes branches principais:

```text
main
develop
feature/*
fix/*
```

### `main`

Contém a versão mais estável do projeto.

Não devem ser feitas alterações diretamente nesta branch.

### `develop`

É utilizada para integração do trabalho realizado pela equipa.

### `feature/*`

Cada nova funcionalidade ou tarefa deverá ser desenvolvida numa branch própria criada a partir da `develop`.

Exemplos:

```text
feature/database-setup
feature/backend-setup
feature/frontend-setup
feature/auth
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
feature/nome-da-tarefa
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

Os membros da equipa devem evitar alterações diretas na `main`.

Sempre que possível, um Pull Request deverá ser revisto por pelo menos outro membro da equipa antes do merge.

## Convenção de Commits

Exemplos:

```text
feat: adicionar funcionalidade de login
fix: corrigir validação do formulário
docs: atualizar documentação
test: adicionar testes
refactor: reorganizar código
chore: configurar projeto
```


## Gestão de Tarefas

As tarefas são organizadas através de **GitHub Issues** e do **GitHub Project Board**.

Estados utilizados:

```text
Todo
In Progress
Review
Done
```

Cada membro é responsável por atualizar o estado das suas tarefas.

## Definition of Done

Uma tarefa poderá ser considerada concluída quando:

* A implementação estiver funcional
* Tiver sido testada localmente
* Não existirem erros críticos conhecidos
* O Pull Request tiver sido criado
* O trabalho tiver sido revisto
* A alteração tiver sido integrada na branch adequada
* A documentação relevante tiver sido atualizada, quando necessário


## Prazo

Prazo total do projeto:

**2 semanas**

## Organização

Projeto desenvolvido no âmbito da iniciativa **Build & Learn IT**.
