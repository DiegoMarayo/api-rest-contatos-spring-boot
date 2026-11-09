# API REST de Contatos — Spring Boot

API REST desenvolvida em Java com Spring Boot para gerenciamento de contatos, permitindo realizar operações de cadastro, consulta, atualização e exclusão de registros.

O projeto foi desenvolvido como atividade prática da disciplina **Desenvolvimento Web - Back End**, com o objetivo de aplicar conceitos de desenvolvimento de APIs REST, persistência de dados e integração com banco de dados relacional.

## 🚀 Tecnologias utilizadas

- Java 17
- Spring Boot 4.1.2
- Spring Web MVC
- Spring Data JPA
- Hibernate
- MySQL
- Maven

## 🏗️ Estrutura do projeto

```text
demorest/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/example/demorest/
│       │       ├── controller/
│       │       │   └── ContatoController.java
│       │       ├── model/
│       │       │   └── Contato.java
│       │       ├── repository/
│       │       │   └── ContatoRepository.java
│       │       └── DemorestApplication.java
│       └── resources/
│           └── application.properties
└── pom.xml
```

## ⚙️ Funcionalidades

A API disponibiliza operações CRUD (*Create, Read, Update e Delete*) para gerenciamento de contatos.

| Método HTTP | Endpoint | Descrição |
|---|---|---|
| GET | `/contatos` | Lista todos os contatos |
| GET | `/contatos/{id}` | Busca um contato pelo ID |
| POST | `/contatos` | Cadastra um novo contato |
| PUT | `/contatos/{id}` | Atualiza um contato |
| DELETE | `/contatos/{id}` | Exclui um contato |

## 🗄️ Banco de dados

O projeto utiliza MySQL para armazenamento dos dados e Spring Data JPA com Hibernate para realizar o mapeamento objeto-relacional (ORM).

Banco de dados utilizado:

```text
bd_rest
```

Configure as credenciais de acesso ao MySQL no arquivo:

`src/main/resources/application.properties`

Exemplo de configuração:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/bd_rest
spring.datasource.username=root
spring.datasource.password=SUA_SENHA

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
```

Substitua `SUA_SENHA` pela senha configurada no seu MySQL.

## ▶️ Como executar o projeto

**Pré-requisitos:**
- JDK 17 ou superior.
- MySQL Server instalado e em execução.
- Maven.

**1. Clone o repositório**

```bash
git clone https://github.com/SEU-USUARIO/api-rest-contatos-spring-boot.git
```

**2. Acesse a pasta do projeto**

```bash
cd api-rest-contatos-spring-boot
```

**3. Configure o banco de dados**

Crie o banco `bd_rest` no MySQL e configure as credenciais no `application.properties`.

**4. Execute a aplicação**

```bash
./mvnw spring-boot:run
```

No Windows:

```bash
mvnw.cmd spring-boot:run
```

A API ficará disponível em:

```text
http://localhost:8080
```

## 🧪 Testando a API

As requisições podem ser realizadas utilizando ferramentas como:

- Postman
- Insomnia
- cURL

Exemplo de consulta:

```http
GET http://localhost:8080/contatos
```

Exemplo de cadastro:

```http
POST http://localhost:8080/contatos
Content-Type: application/json
```

O corpo JSON deve seguir os atributos definidos na classe `Contato`.

## 📚 Conceitos aplicados

- Desenvolvimento de APIs REST.
- Arquitetura cliente-servidor.
- Mapeamento objeto-relacional com JPA/Hibernate.
- Persistência de dados em MySQL.
- Utilização de métodos HTTP.
- Manipulação de dados no formato JSON.
- Organização do código em camadas de Controller, Model e Repository.

## 🎯 Objetivo do projeto

Consolidar conhecimentos de desenvolvimento Back-end com Java e Spring Boot, aplicando os principais conceitos necessários para construção de APIs REST integradas a bancos de dados relacionais.

---

**Projeto acadêmico — Engenharia de Software**

Desenvolvido como prática de estudos em Java Back-end e Spring Boot.