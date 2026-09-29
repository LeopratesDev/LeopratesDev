## Olá, eu sou o Leonardo Prates

**Desenvolvedor Full Stack Júnior** | C# · .NET · Node.js · NestJS · React · TypeScript · SQL

Formado em Análise e Desenvolvimento de Sistemas (UNIP, 2023). Antes de programar, trabalhei com atendimento (SAC) e suporte técnico. Busco uma vaga de desenvolvedor júnior full stack ou back-end (.NET ou Node.js) em São Paulo.

### Stack

| Área | Tecnologias |
|---|---|
| Back-end | C#, ASP.NET Core, Entity Framework Core, Node.js, NestJS, APIs REST, JWT |
| Front-end | React, TypeScript, React Router, TanStack Query, Tailwind CSS |
| Banco de dados | SQL Server, PostgreSQL, Prisma, modelagem relacional, migrations |
| Filas e IA | BullMQ + Redis (workers, retry, jobs agendados), integração com LLM (Claude API) |
| Testes | xUnit, FluentAssertions, Jest, Testcontainers, Vitest, Testing Library |
| DevOps | Git, GitHub Actions, Docker, Docker Compose, Azure App Service, Azure SQL |

### Projetos em destaque

**[RH Manager](https://github.com/LeopratesDev/rh-manager)**: sistema de gestão de RH com funcionários, departamentos e férias com fluxo de aprovação.
[Demo online](https://leopratesdev.github.io/rh-manager/) · [Documentação da API](https://rh-manager-api-nmsbk.azurewebsites.net/scalar/v1)

- API REST em C# / .NET 10 com arquitetura em camadas, SQL Server, autenticação JWT e papéis Admin e Colaborador.
- Front em React + TypeScript com formulários validados por Zod e rotas protegidas por papel.
- 172 testes automatizados e CI com 3 jobs a cada pull request.
- Deploy contínuo no Azure e no GitHub Pages, sem segredos no repositório (OIDC e identidade gerenciada).

**[HelpDesk API](https://github.com/LeopratesDev/helpdesk-api)**: API de chamados com triagem por IA. Eu atendia chamados; agora construí o sistema que os organiza.

- API REST em Node.js / NestJS com TypeScript strict, PostgreSQL + Prisma e 26 endpoints documentados no Swagger.
- Triagem assíncrona: o chamado é criado em ~10 ms e um worker (BullMQ + Redis) chama o Claude com timeout, retry com backoff, validação Zod e processamento idempotente; modo fake para rodar sem chave.
- SLA por prioridade com job agendado, máquina de status auditada e métricas de acerto da IA.
- 157 testes (Jest + Testcontainers com PostgreSQL e Redis reais), 97% de cobertura nas regras de negócio e `docker compose up` com API, worker, banco e Redis.

### Contato

- LinkedIn: [linkedin.com/in/leonardo-prates77](https://www.linkedin.com/in/leonardo-prates77/)
- E-mail: lp.prates7@gmail.com
