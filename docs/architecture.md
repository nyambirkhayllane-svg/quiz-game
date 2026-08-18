# Arquitetura do Projeto

## Visão Geral

O Quiz Game Platform segue uma arquitetura cliente-servidor.

O frontend comunica com o backend através de uma API REST utilizando HTTP e JSON.

## Fluxo da Arquitetura

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

## Frontend

Tecnologias:

- HTML5
- CSS3
- JavaScript

Estrutura principal:

- pages/
- css/
- js/
- assets/

## Backend

Tecnologias:

- Java 21
- Spring Boot
- Spring Web
- Spring Data JPA
- Spring Security
- Maven

Principais pacotes:

- controller
- service
- repository
- model
- dto
- security
- config
- exception

## Base de Dados

Base de dados utilizada:

- PostgreSQL

Camada de acesso a dados:

- Spring Data JPA
- Hibernate

## Autenticação

A autenticação será implementada com:

- Spring Security
- JWT

## Fluxo Git

Branches principais:

- main
- develop
- feature/*
- fix/*

As novas funcionalidades devem ser criadas a partir da branch `develop`.

Depois de concluídas, devem ser integradas através de Pull Requests.

A branch `main` deve conter apenas versões estáveis do projeto.

## Fluxo de Desenvolvimento

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
