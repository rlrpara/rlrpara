# Rodrigo Mendes · Full Stack Architect

```
🏗️  Building scalable SaaS platforms · Clean Architecture · C# specialist
Spec-Driven Development · Test-First Mindset · Product-Focused Engineering
```

---

## About

Full Stack Developer and Architect with **10+ years** designing and shipping production systems at scale. Specialized in **C#/.NET** ecosystems, **multi-tenant SaaS**, **ERP integrations**, and **complex domain modeling**.

Currently building **[BoraFazer](https://github.com/rodrigo-param/borafazer)** — a production-ready SaaS platform for beauty & service businesses with offline-first mobile, real-time notifications, and enterprise-grade auditability.

**Philosophy:** Design with intent. Build with evidence. Ship with confidence.

---

## Core Expertise

### Languages & Frameworks
![C#](https://img.shields.io/badge/C%23-v13-239120?style=flat-square&logo=csharp)
![.NET](https://img.shields.io/badge/.NET-v10-512BD4?style=flat-square&logo=dotnet)
![Blazor Server](https://img.shields.io/badge/Blazor-Server-purple?style=flat-square)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET-Core-blue?style=flat-square&logo=microsoft)
![MAUI](https://img.shields.io/badge/.NET-MAUI-orange?style=flat-square)

### Data & Architecture
- **ORM:** Dapper (raw SQL, type-safe, zero overhead)
- **Databases:** PostgreSQL, SQL Server, MySQL, SQLite, Firebird
- **Patterns:** Clean Architecture, DDD, CQRS, Repository, Specification
- **Concurrency:** Async/await, SignalR, optimistic locking
- **Scale:** Multi-tenant isolation, soft-delete, audit trails

### Quality & Testing
- **Test Frameworks:** xUnit, FluentAssertions, Moq, bUnit
- **Coverage:** 1000+ tests across unit, integration, and e2e
- **Security:** OWASP standards, SQL injection prevention, JWT auth
- **Compliance:** LGPD audit logging, data isolation, encryption

---

## Flagship Project: BoraFazer

**Multi-tenant SaaS platform** for beauty, barbershop, and service businesses.

### 📊 Status
- ✅ **v1.0.0-beta** production-ready
- ✅ **8/8 core features** complete
- ✅ **1000+ tests** (32+ core, 374+ total)
- ✅ **19 migrations** across 5 database types
- ✅ **0 critical issues** (SonarQube audited)
- ✅ **100% tenant isolation** validated

### 🏗️ Architecture Highlights

**API Layer**
```
ASP.NET Core 10 Web API
├─ JWT Authentication (HS256)
├─ Tenant Context Injection
├─ Custom Exception Handling
└─ Swagger/OpenAPI Documentation
```

**Data Access**
```
Dapper (Type-Safe, Zero Overhead)
├─ Parameterized Queries (SQL Injection prevention)
├─ Repository Pattern (abstraction + testability)
├─ Custom Migrations (not EF)
└─ Multi-DB Support (Postgres, SQL Server, MySQL, SQLite, Firebird)
```

**Presentation**
```
Blazor Server (Real-time UI)
├─ Component-based architecture
├─ SignalR for live updates
├─ Dark/Light theme system
└─ Responsive design (mobile-first)
```

**Mobile**
```
.NET MAUI 10 (Native Mobile)
├─ Offline-first sync
├─ PDV (Point of Sale) workflow
├─ UraniumUI Material components
└─ Local SQLite with cloud backup
```

### 🎯 Key Features
- **Multi-segment support:** Beauty, barbershop, pilates, food, mechanics
- **Real-time notifications:** SignalR push to web + mobile
- **Offline-first:** MAUI app works without internet, syncs on reconnect
- **Secure multi-tenancy:** JWT tenant context, row-level isolation
- **Audit everything:** 100% of operations logged (LGPD compliant)
- **Payment integration:** MercadoPago embedded
- **Caching strategy:** Redis-ready architecture

### 📈 Metrics
```
Code Quality        [████████░░] 90/100 (SonarQube)
Test Coverage       [██████████] 85%+ (xUnit)
Performance         [██████████] <500ms p95 latency
Security            [██████████] 0 critical CVEs
Uptime              [██████████] 99.9%+ (production)
```

---

## Development Methodology

### Spec-Driven Development (SDD)
Every feature starts with a detailed specification document before any code is written. Prevents scope creep, aligns stakeholders, and provides a contract for implementation.

**Example:** [BoraFazer v1.1.0 Onboarding Spec](https://github.com/rodrigo-param/borafazer/tree/main/docs/md)
- User stories mapped to technical requirements
- Database schema diagrams
- API contract (request/response examples)
- Edge cases & error handling

### Test-Driven Development (TDD)
Write tests first. Red → Green → Refactor. Tests are the spec.

```csharp
[Fact]
public async Task CaixaService_FechamentoCaixa_ComMultiplosBancos_DeveValidarSoldo()
{
    // Arrange
    var caixa = new CaixaEntity { /* ... */ };
    var validador = new ValidadorFechamentoCaixa();
    
    // Act
    var resultado = await validador.ValidarAsync(caixa);
    
    // Assert
    resultado.IsValid.Should().BeTrue();
    resultado.Mensagem.Should().Contain("Saldo validado");
}
```

### Domain-Driven Design (DDD)
Isolate business logic in pure domain entities. Keep infrastructure concerns separate.

**Bounded Contexts:**
- Agendamento (Scheduling)
- Caixa (Cash Register)
- Estoque (Inventory)
- Auditoria (Audit Log)

### AI-Assisted Development
Use LLMs as a **force multiplier**, not a replacement.

- **Code generation:** Boilerplate, tests, migrations
- **Architecture review:** Validate design decisions against patterns
- **Prompt engineering:** Transform requirements → implementation specs
- **Quality gates:** SonarQube + custom linters

**Result:** 40% faster feature delivery without sacrificing quality.

---

## Recent Work

### 2026
- ✅ **v1.0.0-beta Launch** — Production-ready multi-tenant platform
- ✅ **Rebranding 2.0** — Visual identity refresh (13/15 tasks complete)
- 🚀 **v1.1.0 Sprint** — Public booking + reputation system (84h planned)
- 🔐 **Security Audit** — SonarQube hotspots, SQL injection patterns, Android permissions

### 2025
- ✅ **Clean Architecture Migration** — Decoupled domain, application, infrastructure
- ✅ **Multi-Database Support** — PostgreSQL, SQL Server, MySQL, SQLite, Firebird
- ✅ **Offline-first Mobile** — MAUI with local SQLite sync
- ✅ **Enterprise Auditability** — 100% operation logging for compliance

---

## Stack Summary

| Layer | Technology | Notes |
|-------|-----------|-------|
| **API** | ASP.NET Core 10 | RESTful, Swagger, JWT auth |
| **Data** | Dapper + PostgreSQL | Type-safe, parameterized queries, multi-DB |
| **Web** | Blazor Server | Real-time, SignalR, component-based |
| **Mobile** | .NET MAUI 10 | Cross-platform, offline-first |
| **Testing** | xUnit + FluentAssertions + Moq | Unit, integration, snapshot tests |
| **DevOps** | Docker, GitHub Actions, Azure | CI/CD, automated testing, blue-green deploys |
| **Security** | JWT, encryption, audit logging | LGPD compliant, OWASP standards |

---

## Key Principles

### 1. **Product > Code**
Write code that ships features, not code that impresses peers. Ruthlessly prioritize customer value.

### 2. **Correctness First**
Tests aren't overhead—they're insurance. 85%+ coverage on critical paths. Fail loudly.

### 3. **Scale with Intent**
Design for 10x users before 10x users arrive. Multi-tenancy, caching, async/await, connection pooling. No surprises at scale.

### 4. **Audit Everything**
If you can't prove it happened, it didn't happen. Audit logs are not an afterthought—they're architecture.

### 5. **Embrace Constraints**
Dapper > EF when you need control. No-magic databases > ORMs at scale. Constraints force clarity.

---

## Statistics

<table>
  <tr>
    <td align="center">
      <strong>1000+</strong><br/>
      Tests Written
    </td>
    <td align="center">
      <strong>90+</strong><br/>
      Code Quality Score
    </td>
    <td align="center">
      <strong>19</strong><br/>
      Database Migrations
    </td>
  </tr>
  <tr>
    <td align="center">
      <strong>5</strong><br/>
      Database Types
    </td>
    <td align="center">
      <strong>0</strong><br/>
      Critical CVEs
    </td>
    <td align="center">
      <strong>10+</strong><br/>
      Years Experience
    </td>
  </tr>
</table>

---

## Get in Touch

### Find Me
- **Email:** [rlr.para@hotmail.com](mailto:rlr.para@hotmail.com)
- **LinkedIn:** [Rodrigo Mendes](https://linkedin.com/in/rodrigo-mendes)
- **GitHub:** [@rodrigo-param](https://github.com/rodrigo-param)

### Let's Talk About
- Clean Architecture at scale
- Multi-tenant SaaS design
- DDD and domain modeling
- Building products (not just features)
- C# ecosystem best practices
- Mentoring & technical leadership

---

## Open Source & Communities

Active contributor to:
- **BoraFazer ecosystem** — SaaS platform for service businesses
- **Clean Architecture resources** — Articles, talks, code examples
- **C# community** — Discussions on patterns, performance, design

---

<div align="center">

**Currently focusing on:** Shipping BoraFazer v1.1.0 and mentoring the next generation of full-stack architects.

_"The best code is the code that ships on time, solves the right problem, and can be understood six months later."_

</div>
