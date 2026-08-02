# Arquitetura do Sistema - Nexus Manager

## Visão geral

O Nexus Manager será desenvolvido seguindo uma arquitetura Full Stack, separando a aplicação em três camadas principais:

- Front-end
- Back-end
- Banco de dados

---

## Estrutura da aplicação
Usuário

↓

Front-end
React + TypeScript

↓

API REST
Node.js + Express

↓

Banco de Dados
PostgreSQL + Prisma


---

## Front-end

Responsável pela interface que o usuário utiliza.

Tecnologias:

- React
- TypeScript
- Tailwind CSS

Responsabilidades:

- Exibir telas
- Enviar informações para a API
- Controlar navegação
- Apresentar dados e gráficos

---

## Back-end

Responsável pelas regras do sistema.

Tecnologias:

- Node.js
- Express
- TypeScript
- Prisma ORM

Responsabilidades:

- Criar API REST
- Autenticar usuários
- Validar informações
- Gerenciar regras de negócio

---

## Banco de dados

Responsável pelo armazenamento das informações.

Tecnologia:

- PostgreSQL

Principais tabelas:

- Users
- Clients
- Products
- Sales
- Sale_items

---

## Comunicação entre as camadas

O usuário acessa o sistema pelo Front-end.

O Front-end envia solicitações para a API.

A API processa as regras e consulta o banco de dados.

O resultado retorna para o usuário.

---

## Objetivo da arquitetura

Criar um sistema organizado, escalável e fácil de manter, seguindo boas práticas de desenvolvimento de sof