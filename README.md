# Roadmap de Estudos — C# / .NET

O objetivo deste roadmap é aprender C# e .NET através de prática, evitando conteúdos introdutórios de programação que já são conhecidos.

Cada fase possui projetos práticos. A próxima fase só deve começar quando os conceitos da fase atual estiverem suficientemente consolidados através da implementação.

---

# Fase 1 — C# para quem já programa

**Objetivo:** adquirir fluência na linguagem C#, entendendo as principais diferenças em relação a JavaScript/TypeScript.

**Duração estimada:** 2–3 semanas

## Conteúdos

Sintaxe C#
├── tipos
├── var
├── nullable
├── propriedades
├── fields
├── métodos
├── constructors
├── access modifiers
├── readonly
├── static
├── enums
├── exceptions
└── pattern matching

## Projeto 1 — CLI Task Manager

Uma aplicação de terminal para gerenciamento de tarefas.

### Funcionalidades

- Criar tarefa
- Listar tarefas
- Buscar tarefa por ID
- Marcar tarefa como concluída
- Remover tarefa
- Filtrar tarefas por status

### Objetivo técnico

Praticar:

- tipos
- var
- métodos
- classes
- propriedades
- fields
- constructors
- enum
- nullable
- static
- readonly
- access modifiers

A aplicação deve armazenar os dados apenas em memória.

---

## Projeto 2 — Sistema Bancário

Uma aplicação de terminal simulando operações bancárias.

### Funcionalidades

- Criar conta
- Consultar saldo
- Depositar
- Sacar
- Transferir entre contas
- Exibir histórico de operações

### Regras

- Não permitir depósito com valor inválido
- Não permitir saque maior que o saldo
- Não permitir transferência para a própria conta
- Não permitir valores negativos
- Conta deve possuir um estado válido

### Objetivo técnico

Praticar:

- encapsulamento básico
- constructors
- fields privados
- propriedades
- readonly
- métodos
- exceptions
- enums
- nullable
- pattern matching

---

## Projeto 3 — Sistema de Inventário

Uma aplicação de terminal para gerenciamento de estoque.

### Funcionalidades

- Cadastrar produto
- Listar produtos
- Buscar produto
- Alterar preço
- Adicionar estoque
- Remover estoque
- Consultar quantidade disponível

### Regras

- Produto deve possuir nome
- Preço não pode ser negativo
- Estoque não pode ficar negativo
- Produto inexistente deve gerar erro apropriado
- Operações inválidas devem ser rejeitadas

### Objetivo técnico

Consolidar:

- classes
- propriedades
- fields
- constructors
- métodos
- access modifiers
- exceptions
- enums
- nullable
- pattern matching
- organização básica de código

Ao terminar este projeto, você deve conseguir ler e escrever C# básico sem precisar traduzir mentalmente para TypeScript.

---

# Fase 2 — POO + C# intermediário

**Objetivo:** aprender a utilizar C# para modelar sistemas através de objetos e abstrações.

**Duração estimada:** 2–4 semanas

## Conteúdos

POO
├── encapsulamento
├── abstração
├── herança
├── polimorfismo
├── interfaces
├── composição
└── classes abstratas

C#
├── generics
├── collections
├── LINQ
├── delegates
├── lambdas
└── extension methods

## Projeto 1 — Sistema de Biblioteca

Sistema para gerenciamento de livros, usuários e empréstimos.

### Entidades principais

Book
Member
Loan

### Funcionalidades

- Cadastrar livro
- Cadastrar membro
- Emprestar livro
- Devolver livro
- Consultar livros disponíveis
- Consultar livros emprestados
- Consultar empréstimos de um membro

### Regras

- Livro indisponível não pode ser emprestado
- Membro não pode possuir mais que determinado número de empréstimos
- Um empréstimo deve possuir data de retirada
- Um livro devolvido volta a ficar disponível

### Objetivo técnico

Praticar:

- encapsulamento
- composição
- interfaces
- abstração
- collections
- generics
- LINQ
- exceptions

---

## Projeto 2 — Sistema de Pagamentos

Sistema capaz de processar diferentes formas de pagamento.

### Formas de pagamento

CreditCardPayment
PixPayment
BankTransferPayment

Todas devem possuir um comportamento comum de pagamento.

### Funcionalidades

- Processar pagamento
- Consultar status
- Cancelar pagamento
- Listar pagamentos realizados

### Regras

Cada forma de pagamento possui comportamentos específicos.

Exemplo:

Pix
├── processa imediatamente
└── não possui parcelamento

Cartão
├── pode parcelar
└── possui limite

Transferência
└── depende de confirmação

### Objetivo técnico

Praticar profundamente:

- interfaces
- classes abstratas
- herança
- polimorfismo
- abstração
- composição
- generics
- delegates
- lambdas

O objetivo não é simplesmente criar três classes.

O objetivo é entender quando objetos diferentes podem ser tratados através de uma mesma abstração.

---

## Projeto 3 — Sistema de Relatórios

Aplicação que recebe diferentes tipos de dados e gera relatórios.

### Funcionalidades

- Gerar relatório de vendas
- Gerar relatório de clientes
- Gerar relatório de produtos
- Filtrar dados
- Ordenar dados
- Agrupar dados
- Calcular totais e estatísticas

### Objetivo técnico

Foco principal em:

- Collections
- Generics
- LINQ
- lambdas
- delegates
- extension methods

Exercitar operações como:

- Where
- Select
- OrderBy
- ThenBy
- GroupBy
- Any
- All
- First
- FirstOrDefault
- Single
- SingleOrDefault
- Count
- Sum
- Average

Ao terminar a Fase 2, você deve estar confortável com a modelagem de objetos em C# e com as principais ferramentas da linguagem utilizadas no desenvolvimento de aplicações reais.

---

# Fase 3 — ASP.NET Core

**Objetivo:** aprender a construir backends reais utilizando ASP.NET Core Web API.

ASP.NET Core
├── Web API
├── Controllers
├── Routing
├── Dependency Injection
├── Configuration
├── Middleware
├── HTTP
├── DTOs
├── Validation
└── Error handling

## Projeto 1 — Product Catalog API

Primeiro contato estruturado com ASP.NET Core.

### Funcionalidades

GET    /api/products
GET    /api/products/{id}
POST   /api/products
PUT    /api/products/{id}
DELETE /api/products/{id}

### Arquitetura

Controller
    ↓
Service
    ↓
In-memory collection

### Objetivos

Aprender:

- criação de Web API
- Controllers
- Routing
- HTTP methods
- status codes
- Dependency Injection
- Services
- Requests
- Responses
- DTOs básicos
- Validation
- tratamento de erros

Ainda sem banco de dados.

---

## Projeto 2 — Help Desk API

Evolução para um sistema com regras de negócio mais relevantes.

### Entidades

Ticket
Technician
User
Comment

### Funcionalidades

- Criar chamado
- Listar chamados
- Consultar chamado
- Atribuir técnico
- Iniciar atendimento
- Adicionar comentário
- Resolver chamado
- Fechar chamado

### Estados

Open
InProgress
Resolved
Closed

### Regras

- Ticket inicia como Open
- Ticket precisa de técnico para iniciar
- Apenas InProgress pode ser Resolved
- Apenas Resolved pode ser Closed
- Ticket Closed não pode voltar para outro estado
- Técnico inativo não pode receber chamados

### Arquitetura

Controller
    ↓
Application Service
    ↓
Domain
    ↓
In-memory repository

### Objetivo

Começar a separar:

HTTP
↓
Application
↓
Domain

E entender por que as regras de negócio não devem ficar dentro dos Controllers.

---

## Projeto 3 — Order Management API

Uma API de gerenciamento de pedidos.

### Entidades

Customer
Order
OrderItem
Product

### Funcionalidades

- Criar pedido
- Adicionar produtos
- Remover produtos
- Consultar pedido
- Calcular total
- Confirmar pedido
- Cancelar pedido
- Listar pedidos do cliente

### Estados

Draft
Confirmed
Cancelled

### Regras

- Pedido deve possuir pelo menos um item para ser confirmado
- Produto deve existir
- Quantidade deve ser maior que zero
- Pedido confirmado não pode receber novos itens
- Pedido cancelado não pode ser confirmado
- Total deve ser calculado a partir dos itens

### Arquitetura

API
 ↓
Application
 ↓
Domain

Persistência ainda pode ser simulada em memória.

### Objetivo

Consolidar:

- ASP.NET Core
- Controllers
- Routing
- DI
- DTOs
- Validation
- Services
- Domain logic
- HTTP
- Error handling
- organização de uma Web API

---

# Fase 4 — Persistência

**Objetivo:** aprender como aplicações .NET persistem e consultam dados utilizando Entity Framework Core e PostgreSQL.

Entity Framework Core
├── DbContext
├── Entities
├── Relationships
├── Migrations
├── Queries
├── Tracking
└── PostgreSQL

## Projeto 1 — Product Catalog + Database

Evoluir o Product Catalog API da Fase 3.

Substituir:

In-memory collection

por:

ASP.NET Core
      ↓
EF Core
      ↓
PostgreSQL

### Funcionalidades

- CRUD de produtos
- Busca por nome
- Filtro por categoria
- Ordenação
- Paginação

### Objetivos

Aprender:

- DbContext
- DbSet
- Entity configuration
- conexão com PostgreSQL
- migrations
- criação do banco
- consultas
- inserção
- atualização
- remoção
- tracking

---

## Projeto 2 — Order Management + Database

Evoluir o Order Management API.

### Relacionamentos

Customer
   │
   └── Orders
          │
          └── OrderItems
                  │
                  └── Product

### Objetivos

Aprender:

- relacionamentos 1:N
- relacionamentos N:1
- foreign keys
- navigation properties
- migrations
- queries com relacionamentos
- Include
- ThenInclude
- projeções com LINQ
- tracking vs no-tracking

---

## Projeto 3 — SupportSystem

Projeto principal de consolidação.

O SupportSystem será a evolução dos conhecimentos adquiridos nas fases anteriores.

### Domínio

User
Technician
Ticket
Comment

### Arquitetura

SupportSystem
│
├── SupportSystem.Api
├── SupportSystem.Application
├── SupportSystem.Domain
└── SupportSystem.Infrastructure

Fluxo:

HTTP
 ↓
API
 ↓
Application
 ↓
Domain
 ↓
Infrastructure
 ↓
EF Core
 ↓
PostgreSQL

### Funcionalidades

#### Tickets

- Criar
- Consultar
- Listar
- Atribuir técnico
- Iniciar
- Resolver
- Fechar
- Cancelar

#### Técnicos

- Cadastrar
- Ativar
- Desativar
- Listar
- Consultar chamados atribuídos

#### Usuários

- Cadastrar
- Listar
- Consultar
- Consultar chamados criados

#### Comentários

- Adicionar comentário
- Listar histórico do chamado

### Regras de negócio

Open
 ↓
InProgress
 ↓
Resolved
 ↓
Closed

- Ticket precisa de técnico para iniciar
- Técnico inativo não pode receber novos tickets
- Ticket resolvido pode ser fechado
- Ticket fechado não pode ser alterado
- Comentários precisam possuir autor
- Comentários precisam estar associados a um Ticket
- Ticket deve possuir título e descrição
- Prioridade deve ser válida
- Operações inválidas devem ser rejeitadas pelo domínio

### Objetivo final

Ao concluir o SupportSystem, você deverá conseguir compreender o fluxo completo:

HTTP Request
     ↓
Controller
     ↓
DTO
     ↓
Application Service
     ↓
Domain
     ↓
Repository / EF Core
     ↓
PostgreSQL
     ↓
Response

E principalmente conseguir explicar por que cada parte existe, em vez de apenas reproduzir uma arquitetura encontrada em um tutorial.

---

# Ordem de Progressão

FASE 1
C# para quem já programa
│
├── CLI Task Manager
├── Sistema Bancário
└── Sistema de Inventário
        │
        ▼
FASE 2
POO + C# intermediário
│
├── Sistema de Biblioteca
├── Sistema de Pagamentos
└── Sistema de Relatórios
        │
        ▼
FASE 3
ASP.NET Core
│
├── Product Catalog API
├── Help Desk API
└── Order Management API
        │
        ▼
FASE 4
Persistência
│
├── Product Catalog + PostgreSQL
├── Order Management + PostgreSQL
└── SupportSystem

# Regra de Estudo

Para cada projeto:

1. Entender o problema
2. Definir as regras
3. Tentar implementar sozinho
4. Encontrar dificuldades
5. Estudar o conceito necessário
6. Implementar
7. Refatorar
8. Revisar o que foi aprendido
9. Avançar

A IA deve ser utilizada como professor, revisor e ferramenta de investigação, e não como substituta da implementação.

Antes de pedir uma implementação completa, tentar resolver o problema sozinho e utilizar a IA principalmente para entender erros, conceitos desconhecidos, decisões de design e alternativas.
