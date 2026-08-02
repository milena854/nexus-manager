# Modelo de Banco de Dados - Nexus Manager

## Visão geral

O Nexus Manager utiliza um banco de dados relacional PostgreSQL para armazenar informações de usuários, clientes, produtos e vendas.

---

# Entidades principais

## Users

Armazena os usuários que acessam o sistema.

Campos:

- id
- name
- email
- password
- role
- created_at


---

## Clients

Armazena os clientes cadastrados.

Campos:

- id
- name
- email
- phone
- company
- created_at


---

## Products

Armazena os produtos disponíveis.

Campos:

- id
- name
- category
- price
- quantity
- created_at


---

## Sales

Armazena as vendas realizadas.

Campos:

- id
- client_id
- user_id
- total
- created_at


---

## Sale_items

Armazena os produtos de cada venda.

Campos:

- id
- sale_id
- product_id
- quantity
- price


---

# Relacionamentos

## Users → Sales

Um usuário pode registrar várias vendas.

Relacionamento:

One-to-Many


## Clients → Sales

Um cliente pode possuir várias vendas.

Relacionamento:

One-to-Many


## Sales → Sale_items

Uma venda pode possuir vários produtos.

Relacionamento:

One-to-Many


## Products → Sale_items

Um produto pode aparecer em várias vendas.

Relacionamento:

One-to-Many


---

# Objetivo do modelo

Criar uma estrutura organizada, evitando duplicação de dados e permitindo que o sistema cresça futuramente.