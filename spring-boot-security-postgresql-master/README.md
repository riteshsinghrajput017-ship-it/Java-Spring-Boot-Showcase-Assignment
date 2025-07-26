# 📡 Public API Gateway App – Consumer & Dashboard Portal

A full-stack Spring Boot application where users can:

-  Sign up and log in using **JWT token-based authentication**
-  Add URLs of **public JSON APIs**
-  Fetch and **store responses** of those APIs under their profile
-  View a personal **dashboard** of saved API responses

Each user can only access **their own saved URLs and results**.

---

##  Tech Stack

| Layer         | Technology               |
|---------------|--------------------------|
| Backend       | Java (Spring Boot)       |
| Auth          | JWT (JSON Web Tokens)    |
| Database      | PostgreSQL               |
| ORM           | Spring Data JPA / Hibernate |
| Build Tool    | Maven or Gradle          |
| Server Port   | 8088                     |
| API Protocol  | REST (JSON)              |

---

##  Configuration & Setup

Before running the application, ensure you have configured the following environment or application variables.

You can define them in:

- `.env` file (if you're using dotenv support)
- `application.properties` (for Spring Boot apps)
- Directly in your deployment environment

---

###  Environment Variables

| Variable Name        | Description |
|----------------------|-------------|
| `DB_URL`             | JDBC connection string to your PostgreSQL database. <br> Example: `jdbc:postgresql://localhost:5432/testdb` |
| `DB_USERNAME`        | Username to connect to your PostgreSQL DB. <br> Default: `postgres` |
| `DB_PASSWORD`        | Password to connect to your PostgreSQL DB. <br> Default: `postgres` |
| `JWT_EXPIRATION_MS`  | Validity period for JWT tokens in milliseconds. <br> `86400000` = 24 hours |
| `SERVER_PORT`        | The port number on which the Spring Boot server will run. <br> Default: `8088` |

---

###  Sample `application.properties`

```properties
# PostgreSQL DB Config
spring.datasource.url=jdbc:postgresql://localhost:5432/testdb
spring.datasource.username=postgres
spring.datasource.password=postgres
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.PostgreSQLDialect

# JWT Config
jwt.expiration.ms=86400000

# Server Config
server.port=8088
