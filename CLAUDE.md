# CLAUDE.md

## Visao geral

Projeto educacional com duas implementacoes paralelas de Spring Security: uma em **Java** (Maven) e outra em **Kotlin** (Gradle). Ambas usam Spring Boot 4.0.1 e Java 21.

## Estrutura

```
spring-security-with-java/   # Maven  — pom.xml
spring-security-with-kotlin/  # Gradle — build.gradle.kts
```

Pacotes base:
- Java: `com.restful.spring.security.with.java`
- Kotlin: `com.restful.spring.security.with.kotlin`

## Comandos

### Java (Maven)
```bash
cd spring-security-with-java
./mvnw clean package   # build
./mvnw test            # testes
./mvnw spring-boot:run # rodar
```

### Kotlin (Gradle)
```bash
cd spring-security-with-kotlin
./gradlew build    # build
./gradlew test     # testes
./gradlew bootRun  # rodar
```

## Stack

| Componente | Versao |
|---|---|
| Spring Boot | 4.0.1 |
| Java | 21 |
| Kotlin | 2.2.21 |
| Testes | JUnit 5 |

Dependencias principais: `spring-boot-starter-security`, `spring-boot-starter-security-oauth2-resource-server`, `spring-boot-starter-webmvc`, `spring-boot-starter-validation`, `spring-boot-starter-actuator`.

## Convencoes

- Manter paridade funcional entre as duas implementacoes (Java e Kotlin).
- Toda feature nova deve ser implementada em ambos os modulos.
- Configuracao via `application.yaml` (nao `.properties`).
- Testes com JUnit 5 e utilitarios do Spring Security Test.
- Kotlin: null-safety estrito (`-Xjsr305=strict`).

## Regras para o Claude

- Ao alterar um modulo, verificar se a mesma alteracao se aplica ao outro.
- Rodar `./mvnw test` (Java) e `./gradlew test` (Kotlin) apos mudancas.
- Nao adicionar dependencias sem pedir confirmacao.
- Manter codigo simples e didatico — este e um projeto educacional.
