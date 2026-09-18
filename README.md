# TalentHub API

API REST para uma vitrine de desenvolvedores, projetos e tecnologias.

## Stack
- Java 21
- Spring Boot 3
- Spring Web
- Spring Data JPA / Hibernate
- PostgreSQL
- Bean Validation
- Swagger / OpenAPI
- Maven
- Postman

## Banco de dados

Crie no PostgreSQL:

```sql
CREATE DATABASE talenthub;
```

Por padrão a aplicação usa:
- host: localhost
- porta: 5432
- banco: talenthub
- usuário: postgres
- senha: postgres

Se sua senha for diferente, altere `application.properties`.

## Executar

No terminal do VS Code:

```bash
mvn spring-boot:run
```

API:
`http://localhost:8080`

Swagger:
`http://localhost:8080/swagger-ui/index.html`

## Endpoints

### Profiles
- POST `/api/profiles`
- GET `/api/profiles/{id}`

### Technologies
- POST `/api/technologies`
- GET `/api/technologies`

### Projects
- POST `/api/projects`
- GET `/api/projects`

## Teste rápido

1. Cadastre um profile.
2. Cadastre as technologies.
3. Cadastre um project usando `profileId` e `technologyIds`.
4. Liste projects.
5. Teste uma requisição inválida para demonstrar validação.

## GitHub

```bash
git init
git add .
git commit -m "feat: cria TalentHub API"
git branch -M main
git remote add origin URL_DO_SEU_GITHUB
git push -u origin main
```

## Estrutura

```text
src/main/java/com/talenthub/api
├── controller
├── dto
├── entity
├── exception
├── repository
└── service
```
