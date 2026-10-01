## Olá, eu sou o Leonardo Prates

**Desenvolvedor Back-end Júnior** | C# · .NET · Node.js · React · TypeScript · PostgreSQL

Formado em Análise e Desenvolvimento de Sistemas (UNIP, 2023). Antes de programar, trabalhei com atendimento (SAC) e suporte técnico. Busco uma vaga de desenvolvedor júnior back-end ou full stack em São Paulo.

### Stack

| Área | Tecnologias |
|---|---|
| Back-end | C#, ASP.NET Core, Entity Framework Core, Clean Architecture, CQRS (MediatR) |
| Back-end (Node) | Node.js, NestJS, TypeScript strict, BullMQ + Redis, Prisma |
| Banco de dados | PostgreSQL, SQL Server, EF Core migrations |
| Arquitetura | Clean Architecture, CQRS, multi-tenancy com Global Query Filters |
| Testes | xUnit, NSubstitute, FluentAssertions, Testcontainers, Jest, Supertest |
| Front-end | React, Next.js 15, TypeScript, TanStack Query, Tailwind CSS, Recharts |
| DevOps | GitHub Actions (CI/CD), Docker, Railway, Vercel, Azure |

### Projetos em destaque

**[service-orders-saas](https://github.com/LeopratesDev/service-orders-saas)** · [Demo](https://service-orders-saas.vercel.app) · [API / Swagger](https://service-orders-api-production.up.railway.app/swagger)

Plataforma multi-tenant de gestão de ordens de serviço com integração de pagamentos Pix.

- **Clean Architecture** com 4 camadas (Domain / Application / Infrastructure / API) e dependência unidirecional
- **CQRS via MediatR** — controllers não injetam repositórios, toda lógica passa por commands e queries
- **Multi-tenancy** com EF Core Global Query Filters — isolamento por `TenantId` provado por teste automatizado
- **Máquina de estados** explícita no domínio: Draft → Pending → Paid / Cancelled (DomainException em transições inválidas)
- **Idempotência em pagamentos** com `IdempotencyKey` e índice único filtrado no banco
- **Resiliência** com Polly: retry exponencial (3×) + circuit breaker (5 falhas / 30 s) no gateway Mercado Pago
- **Rate limiting** built-in .NET 7: sliding window 60 req/min geral, 10 req/min em `/auth`
- **35 testes** — 29 unitários (xUnit + NSubstitute) + 6 de integração (Testcontainers, PostgreSQL real)
- **CI/CD** via GitHub Actions: unit tests → integration tests → Railway deploy automático

**[RH Manager](https://github.com/LeopratesDev/rh-manager)** · [Demo](https://leopratesdev.github.io/rh-manager/) · [API](https://rh-manager-api-nmsbk.azurewebsites.net/scalar/v1)

Sistema de gestão de RH com funcionários, departamentos e fluxo de aprovação de férias.

- API REST em C# / .NET 10 com autenticação JWT e papéis Admin/Colaborador
- 172 testes e CI com 3 jobs; deploy no Azure com OIDC (sem segredos no repositório)

**[HelpDesk API](https://github.com/LeopratesDev/helpdesk-api)**

API de chamados com triagem por IA — construída a partir da experiência com atendimento ao cliente.

- API REST em Node.js / NestJS com TypeScript strict, PostgreSQL + Prisma e 26 endpoints documentados no Swagger
- Triagem assíncrona: o chamado é criado em ~10 ms e um worker (BullMQ + Redis) chama o Claude com timeout, retry e validação Zod
- SLA por prioridade com job agendado, máquina de status auditada e métricas de acerto da IA
- 157 testes (Jest + Testcontainers com PostgreSQL e Redis reais), 97% de cobertura nas regras de negócio

### Contato

- LinkedIn: [linkedin.com/in/leonardo-prates77](https://www.linkedin.com/in/leonardo-prates77/)
- E-mail: lp.prates7@gmail.com
