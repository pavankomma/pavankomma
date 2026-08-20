<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg">
  <img src="assets/header-light.svg" alt="Pavan Kumar Komma — Software Architect & Principal Engineer. Enterprise platforms, cloud and distributed systems, applied AI." width="100%">
</picture>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-pavankomma-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/pavankomma)
[![GitHub](https://img.shields.io/badge/GitHub-pavankomma-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/pavankomma)
[![Open to Architect roles](https://img.shields.io/badge/Open_to-Architect_%26_Principal_Engineer_roles-8B5CF6?style=flat-square)](https://linkedin.com/in/pavankomma)

</div>

## Who I am

I'm a **Software Architect and hands-on Principal Engineer with 15+ years of experience** designing, building, securing and operating enterprise platforms for public-sector agencies, legal and compliance organisations, payments, telecom and higher education.

I work across the entire engineering lifecycle — **Domain → Architecture → APIs → Data → Cloud → Security → CI/CD → Production** — and I don't treat architecture as diagrams disconnected from implementation. I work from business boundaries through technical design, production code, infrastructure, delivery pipelines and operational concerns.

The last few years have added a second specialisation: **applied AI inside enterprise systems** — RAG, document intelligence, tool-using agents, text-to-SQL and MCP — engineered with the same requirements for reliability, security, observability, cost and maintainability as conventional software.

> **Enterprise architecture + hands-on engineering + security + production AI** — that combination is what I bring to a team.

## At a glance

| Area | Focus |
|---|---|
| **Role** | Software Architect · Technical Lead · hands-on Principal Engineer |
| **Experience** | 15+ years across enterprise and regulated environments (public sector, legal, payments, compliance) |
| **Primary platform** | C# / .NET 10 · ASP.NET Core · Blazor · EF Core · SQL Server · Azure |
| **Additional engineering** | Go (gRPC services) · Python (FastAPI, LangGraph) · TypeScript (React, Angular, Vue) |
| **Cloud** | Azure end to end (landing zones → workloads → observability) · AWS (ECS, RDS, S3, ElastiCache) |
| **Architecture** | DDD · modular monoliths · microservices · CQRS · event-driven systems |
| **Reliability** | Outbox/inbox · sagas · idempotency · retries · circuit breakers · back-pressure |
| **Security** | Entra ID · OAuth 2.0 · OIDC · Managed Identity · Key Vault · zero trust |
| **AI** | RAG · document intelligence · agents · text-to-SQL · MCP · evaluation |
| **Delivery** | GitHub Actions · Azure DevOps · Terraform · Docker · AKS |
| **Observability** | OpenTelemetry · Application Insights · Log Analytics / KQL |

## Why teams bring me in

- **Architecture ownership** — translate complex business requirements into bounded contexts, service boundaries, data ownership and integration contracts.
- **Hands-on execution** — move from architecture decisions to APIs, services, data models, infrastructure and production integrations.
- **Distributed systems** — design for failure using messaging, idempotency, retries, timeouts, compensation, resilience and operational recovery.
- **Cloud platform engineering** — design Azure platforms end to end, with AWS experience where client environments require it.
- **Security by design** — identity, authorisation, least privilege, secrets, zero-trust boundaries and secure delivery are part of the architecture, not a final checklist.
- **Production AI** — build RAG and agentic workflows with retrieval quality, evaluation, guardrails, human approval, observability and cost/latency as requirements.
- **Engineering enablement** — establish reusable patterns, architecture tests, CI/CD quality gates, testing strategies and delivery practices that let several teams move consistently.

## How I structure a platform

> **The simplest architecture that satisfies the requirement wins.** A modular monolith is the default until a boundary earns its own deployment. Microservices, asynchronous messaging and distributed workflows are introduced when they solve a measurable organisational, scalability, reliability or deployment problem.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/architecture-dark.svg">
  <img src="assets/architecture-light.svg" alt="Reference architecture: clients call an API gateway with an OIDC bearer token; the gateway validates and routes to .NET, Go and Python services; services write state and outbox events, publish to a message bus consumed by idempotent workers; data lives in SQL, Cosmos, Redis and Blob stores; an AI layer of LLMs, agents, a vector index and Document Intelligence is reached via structured tool calls; a platform band provides security, observability, runtime, infrastructure and CI/CD." width="100%">
</picture>

Every layer is independently deployable and scalable, secured by identity rather than network position, and instrumented with OpenTelemetry from day one.

## Architecture & distributed systems

| Design | Distribution | Resilience |
|---|---|---|
| Domain-Driven Design — bounded contexts, aggregates, ubiquitous language | Microservices and modular monoliths, chosen per boundary | Retries with exponential backoff and jitter |
| Clean / vertical-slice architecture with explicit dependency direction | Event-driven architecture; CQRS where read/write separation earns it | Circuit breakers, bulkheads, timeouts (Polly v8 pipelines) |
| API design — REST, gRPC, versioning, OpenAPI-first contracts | Sagas and process managers for long-running workflows | Idempotent handlers and deduplication |
| Multi-tenant data isolation and per-tenant configuration | Outbox / inbox for reliable publishing and exactly-once effects | Dead-letter handling and replay strategies |
| Rules and workflow engines for configurable business logic | Eventual consistency with explicit compensation | Rate limiting, back-pressure, graceful degradation |
| Architecture decision records; architecture tests that keep the dependency graph honest | Distributed caching (cache-aside, HybridCache) and horizontal scaling | Health checks, readiness probes, failure isolation |

## Production AI engineering

I build AI features as **systems**, not demos — retrieval quality, cost, latency, safety and observability are engineering requirements.

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/rag-dark.svg">
  <img src="assets/rag-light.svg" alt="RAG and agent pipeline: an offline ingest lane (sources → extract with Document Intelligence → structure-aware chunking → embeddings → vector index) and an online query lane (request → hybrid retrieval with reranking → generation with structured outputs and tool calls → guardrails and evals → human approval → answer), with a bounded repair loop, a revise-with-feedback loop, and confirmed answers saved back as examples." width="100%">
</picture>

| Area | What I build |
|---|---|
| **RAG** | Hybrid retrieval (BM25 + vector), structure- and schema-aware chunking, reranking, citation tracking, offline evaluation sets; retrieval on Azure AI Search, Chroma and SQL Server vector stores |
| **Document intelligence** | Azure AI Document Intelligence and Text Analytics pipelines over legal, claims and scanned document corpora; structured extraction feeding search and downstream workflow automation |
| **Agentic systems** | LangGraph state machines and Semantic Kernel planners with typed tools, bounded retry/repair loops, persistent memory, human-approval gates, guardrails and evaluation |
| **Text-to-SQL** | Read-only database agents with schema-aware generation, SQL validated (`sqlglot`) before execution, and feedback loops from confirmed question → SQL pairs |
| **MCP** | Internal systems and desktop applications exposed through scoped, auditable tools with explicit permissions and identity boundaries — least privilege, not unrestricted access |
| **AI-assisted engineering** | Claude Code and Codex integrated into the lifecycle (design → implementation → review → migration → testing → documentation), governed by repository conventions, skills and automated verification — throughput up, judgment and quality gates intact |

## Security by design

| Identity | Application security | Secure delivery |
|---|---|---|
| Microsoft Entra ID · Auth0 · Okta | Zero-trust architecture; identity over network position | SAST and static analysis in the pipeline |
| OAuth 2.0 · OpenID Connect · JWT | Least-privilege access and explicit authorisation policies | CodeQL and Sonar analyzers as build gates |
| Managed Identity · workload identity federation | Secrets and certificates in Key Vault, rotated | Dependency and package governance |
| ASP.NET Core Identity · multi-tenant isolation | Input validation and sanitisation; secure API boundaries | Architecture tests that fail the build on violations |
| Token validation at the edge (JWKS, scopes) | Threat-aware architecture decisions and reviews | Secrets never in source control |

## Azure, end to end

| Area | Services |
|---|---|
| Foundation | Landing Zones, Management Groups, Subscriptions, Policy, RBAC |
| Networking | VNets, Private Endpoints, Private DNS, NSGs, Application Gateway / WAF, Front Door |
| Compute | App Service, Azure Functions, Container Apps, AKS, Container Registry |
| Data | Azure SQL, Cosmos DB, Blob Storage, Azure Cache for Redis |
| Integration | API Management, Service Bus, Event Grid, Logic Apps |
| AI | Azure OpenAI, AI Foundry, AI Search, AI Document Intelligence, AI Language |
| Identity & secrets | Microsoft Entra ID, Managed Identity, Key Vault, workload identity federation |
| Observability | Application Insights, Log Analytics / KQL, OpenTelemetry exporters, alerts and dashboards |
| Delivery | Azure DevOps Pipelines, GitHub Actions, Terraform, environment promotion with approvals |

**AWS**, where clients run there: ECS on Fargate, ALB, RDS PostgreSQL, ElastiCache Redis, S3, CloudWatch and WAF — provisioned with Terraform modules.

## Engineering quality & delivery

Architecture is incomplete until the system can be tested, deployed and operated safely.

| Quality gates | Testing strategy | Delivery | Operations |
|---|---|---|---|
| `TreatWarningsAsErrors` · `EnforceCodeStyleInBuild` | Unit — xUnit v3, NSubstitute / Moq, AutoFixture / Bogus | Trunk-based feature flow, production release tags | Structured logging (Serilog) and distributed tracing |
| Central package management | Property-based and snapshot testing | Hotfix-from-tag with merge-back; squash merges | Health checks and readiness probes |
| Sonar analyzers · CodeQL | Integration on Testcontainers | Multi-team release trains and coordination | SLO-oriented alerting and dashboards |
| Architecture tests as build gates | Playwright end-to-end with axe accessibility checks | Environment promotion with approvals | Production diagnostics and incident follow-through |
| Dependency and package governance | BenchmarkDotNet for hot paths; performance and load testing | Infrastructure as code with Terraform | Performance engineering and capacity planning |

## Technology stack

Curated on purpose — the architecture and engineering outcomes matter more than the number of tools. Everything below is in regular production use.

**Languages**

![C#](https://img.shields.io/badge/C%23-239120?style=flat-square&logo=csharp&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![SQL](https://img.shields.io/badge/T--SQL_%2F_PL%2FpgSQL-4479A1?style=flat-square)
![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=flat-square)

**Backend & APIs**

![.NET 10](https://img.shields.io/badge/.NET_10-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-5C2D91?style=flat-square&logo=dotnet&logoColor=white)
![EF Core](https://img.shields.io/badge/EF_Core-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![Dapper](https://img.shields.io/badge/Dapper-1E293B?style=flat-square)
![MediatR](https://img.shields.io/badge/MediatR_%2F_Mediator-1E293B?style=flat-square)
![FluentValidation](https://img.shields.io/badge/FluentValidation-1E293B?style=flat-square)
![Polly](https://img.shields.io/badge/Polly_%2F_Http.Resilience-1E293B?style=flat-square)
![SignalR](https://img.shields.io/badge/SignalR-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![gRPC](https://img.shields.io/badge/gRPC-244C5A?style=flat-square)
![REST](https://img.shields.io/badge/REST_%2F_OpenAPI-85EA2D?style=flat-square&logo=swagger&logoColor=black)
![Scalar](https://img.shields.io/badge/Scalar-1E293B?style=flat-square)
![API Versioning](https://img.shields.io/badge/API_Versioning-1E293B?style=flat-square)
![Ocelot](https://img.shields.io/badge/Ocelot_Gateway-1E293B?style=flat-square)
![.NET Aspire](https://img.shields.io/badge/.NET_Aspire-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=white)

**Frontend & desktop**

![Blazor](https://img.shields.io/badge/Blazor_Server-512BD4?style=flat-square&logo=blazor&logoColor=white)
![MudBlazor](https://img.shields.io/badge/MudBlazor-594AE2?style=flat-square)
![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB)
![Angular](https://img.shields.io/badge/Angular-DD0031?style=flat-square&logo=angular&logoColor=white)
![Vue](https://img.shields.io/badge/Vue_3-4FC08D?style=flat-square&logo=vuedotjs&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white)

**Data & caching**

![SQL Server](https://img.shields.io/badge/SQL_Server-CC2927?style=flat-square&logo=microsoftsqlserver&logoColor=white)
![Azure SQL](https://img.shields.io/badge/Azure_SQL-0078D4?style=flat-square)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![Oracle](https://img.shields.io/badge/Oracle-F80000?style=flat-square&logo=oracle&logoColor=white)
![Cosmos DB](https://img.shields.io/badge/Cosmos_DB-0078D4?style=flat-square)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat-square&logo=sqlite&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white)
![HybridCache](https://img.shields.io/badge/HybridCache-1E293B?style=flat-square)
![Blob Storage](https://img.shields.io/badge/Blob_Storage-0078D4?style=flat-square)
![S3](https://img.shields.io/badge/Amazon_S3-569A31?style=flat-square)

**Messaging & background processing**

![Azure Service Bus](https://img.shields.io/badge/Azure_Service_Bus-0078D4?style=flat-square)
![Event Grid](https://img.shields.io/badge/Event_Grid-0078D4?style=flat-square)
![RabbitMQ](https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white)
![Kafka](https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white)
![Hangfire](https://img.shields.io/badge/Hangfire-004D40?style=flat-square)
![Quartz.NET](https://img.shields.io/badge/Quartz.NET-3B5998?style=flat-square)
![Outbox](https://img.shields.io/badge/Outbox_%2F_Inbox-1E293B?style=flat-square)

**AI & agents**

![Azure OpenAI](https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat-square)
![Azure AI Foundry](https://img.shields.io/badge/Azure_AI_Foundry-0078D4?style=flat-square)
![Azure AI Search](https://img.shields.io/badge/Azure_AI_Search-0078D4?style=flat-square)
![Document Intelligence](https://img.shields.io/badge/AI_Document_Intelligence-0078D4?style=flat-square)
![OpenAI](https://img.shields.io/badge/OpenAI_SDK-412991?style=flat-square&logo=openai&logoColor=white)
![Semantic Kernel](https://img.shields.io/badge/Semantic_Kernel-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square&logo=langgraph&logoColor=white)
![Chroma](https://img.shields.io/badge/Chroma-FF6F00?style=flat-square)
![MCP](https://img.shields.io/badge/Model_Context_Protocol-1E293B?style=flat-square)
![Chainlit](https://img.shields.io/badge/Chainlit-1E293B?style=flat-square)
![ONNX Runtime](https://img.shields.io/badge/ONNX_Runtime-005CED?style=flat-square&logo=onnx&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat-square&logo=claude&logoColor=white)
![Codex](https://img.shields.io/badge/OpenAI_Codex-412991?style=flat-square&logo=openai&logoColor=white)

**Cloud, infrastructure & delivery**

![Azure](https://img.shields.io/badge/Azure-0078D4?style=flat-square)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=flat-square)
![Terraform](https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes_%2F_AKS-326CE5?style=flat-square&logo=kubernetes&logoColor=white)
![Container Apps](https://img.shields.io/badge/Container_Apps-0078D4?style=flat-square)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
![Azure DevOps](https://img.shields.io/badge/Azure_DevOps-0078D7?style=flat-square&logo=azuredevops&logoColor=white)
![GitLab CI](https://img.shields.io/badge/GitLab_CI-FC6D26?style=flat-square&logo=gitlab&logoColor=white)

**Observability**

![OpenTelemetry](https://img.shields.io/badge/OpenTelemetry-000000?style=flat-square&logo=opentelemetry&logoColor=white)
![Application Insights](https://img.shields.io/badge/Application_Insights-0078D4?style=flat-square)
![Log Analytics](https://img.shields.io/badge/Log_Analytics_%2F_KQL-0078D4?style=flat-square)
![Serilog](https://img.shields.io/badge/Serilog-1E293B?style=flat-square)
![NLog](https://img.shields.io/badge/NLog-1E293B?style=flat-square)
![Health Checks](https://img.shields.io/badge/Health_Checks-1E293B?style=flat-square)

**Testing & quality**

![xUnit](https://img.shields.io/badge/xUnit_v3-5B2C6F?style=flat-square)
![NSubstitute](https://img.shields.io/badge/NSubstitute_%2F_Moq-1E293B?style=flat-square)
![AutoFixture](https://img.shields.io/badge/AutoFixture_%2F_Bogus-1E293B?style=flat-square)
![Testcontainers](https://img.shields.io/badge/Testcontainers-2496ED?style=flat-square&logo=docker&logoColor=white)
![Architecture tests](https://img.shields.io/badge/NetArchTest_%2F_ArchUnit-1E293B?style=flat-square)
![BenchmarkDotNet](https://img.shields.io/badge/BenchmarkDotNet-1E293B?style=flat-square)
![Playwright](https://img.shields.io/badge/Playwright_%2B_axe-2EAD33?style=flat-square&logo=playwright&logoColor=white)
![SonarQube](https://img.shields.io/badge/Sonar_analyzers-4E9BCD?style=flat-square&logo=sonar&logoColor=white)
![Load testing](https://img.shields.io/badge/Performance_%26_load_testing-F97316?style=flat-square)

**Security & identity**

![Microsoft Entra ID](https://img.shields.io/badge/Microsoft_Entra_ID-0078D4?style=flat-square)
![Auth0](https://img.shields.io/badge/Auth0-EB5424?style=flat-square&logo=auth0&logoColor=white)
![Okta](https://img.shields.io/badge/Okta-007DC1?style=flat-square&logo=okta&logoColor=white)
![ASP.NET Identity](https://img.shields.io/badge/ASP.NET_Core_Identity-512BD4?style=flat-square&logo=dotnet&logoColor=white)
![OAuth2](https://img.shields.io/badge/OAuth_2.0-3C873A?style=flat-square)
![OpenID Connect](https://img.shields.io/badge/OpenID_Connect-F78C40?style=flat-square&logo=openid&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=white)
![Key Vault](https://img.shields.io/badge/Key_Vault-0078D4?style=flat-square)
![Managed Identity](https://img.shields.io/badge/Managed_Identity-0078D4?style=flat-square)
![Multi-tenancy](https://img.shields.io/badge/Multi--tenancy-1E293B?style=flat-square)
![Zero Trust](https://img.shields.io/badge/Zero_Trust-8B5CF6?style=flat-square)

<sub>Also in regular use: Azure AI Text Analytics · Azure Functions · Azure API Management · Stripe, Twilio and SendGrid integrations · QuestPDF, ClosedXML and Open XML document generation · TWAIN / WIA / eSCL device integration · CodeMirror-based editors.</sub>

## Principles

<table>
  <tr>
    <td width="25%" valign="top"><strong>Domain first</strong><br><sub>Model the business problem and its language before choosing frameworks. Technology is selected last, and only for the boundaries that need it.</sub></td>
    <td width="25%" valign="top"><strong>Boundaries are explicit</strong><br><sub>Contexts, contracts and data ownership are written down, versioned and enforced by architecture tests — not tribal knowledge.</sub></td>
    <td width="25%" valign="top"><strong>Design for failure</strong><br><sub>Every dependency will time out, throttle or disappear. Retries, idempotency, circuit breakers and fallbacks are designed in, not patched in.</sub></td>
    <td width="25%" valign="top"><strong>Security is architecture</strong><br><sub>Identity, least privilege and secrets handling are part of the design and the threat model, not middleware added before go-live.</sub></td>
  </tr>
  <tr>
    <td valign="top"><strong>Observability is a feature</strong><br><sub>If a production system cannot explain what it is doing through traces, metrics and structured logs, it is not finished.</sub></td>
    <td valign="top"><strong>Async where it earns its complexity</strong><br><sub>Messaging decouples failure and deployment domains; synchronous calls stay where latency and consistency genuinely require them.</sub></td>
    <td valign="top"><strong>AI augments judgment</strong><br><sub>Models draft, retrieve and verify; engineers own the decision — with evaluation, guardrails and human approval where the risk warrants it.</sub></td>
    <td valign="top"><strong>Simplicity earns complexity</strong><br><sub>A modular monolith beats premature microservices. Complexity is introduced when a measured requirement justifies it, never in anticipation.</sub></td>
  </tr>
</table>

## What I'm looking for

Roles that combine **software architecture, principal-level engineering, cloud platform architecture, distributed systems, application security and AI / agentic engineering** — in environments that value both technical depth and engineering judgment: architecture that survives contact with production.

---

<div align="center">

**Architect for scale. Build for security. Engineer for change.**

[![Let's Connect on LinkedIn](https://img.shields.io/badge/Let's_connect_on_LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/pavankomma)

</div>
