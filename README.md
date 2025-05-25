# 🛡️ Sistema de Controle de EPIs

Este é um sistema simples de **cadastro e listagem de EPIs (Equipamentos de Proteção Individual)**, desenvolvido com **Spring Boot**, **JDBC** e **HTML**. O sistema permite registrar EPIs e consultar todos os cadastros via interface web ou em formato JSON.

## ✨ Funcionalidades

- ✅ Cadastro de EPIs com nome e validade
- 📋 Listagem dos EPIs cadastrados
- 🌐 Interface HTML simples para entrada de dados
- 🧩 Integração com banco de dados MySQL

## 💻 Tecnologias Utilizadas

- Java 17+
- Spring Boot
- Spring JDBC
- HTML/CSS
- MySQL
- Maven

## 📁 Estrutura do Projeto

-projeto-epi/
-├── pom.xml
-├── src/
-│ ├── main/
-│ │ ├── java/com/exemplo/epi/
-│ │ │ ├── Epi.java
-│ │ │ ├── EpiController.java
-│ │ │ └── EpiRepository.java
-│ │ └── resources/
-│ │ ├── static/epis.html
-│ │ └── application.properties


## ⚙️ Configuração do Banco de Dados

-1. Crie o banco de dados:

-```sql
-CREATE DATABASE episdb;
-USE episdb;

-CREATE TABLE epis (
  -id INT AUTO_INCREMENT PRIMARY KEY,
  -nome VARCHAR(100) NOT NULL,
  -validade DATE NOT NULL
-);

-2. Configure o arquivo application.properties:

-spring.datasource.url=jdbc:mysql://localhost:3306/episdb
-spring.datasource.username=root
-spring.datasource.password=
-spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver


## 🚀 Como Executar

-1. Clone o repositório:

-git clone https://github.com/seu-usuario/nome-do-repo.git
-cd nome-do-repo

-2. Execute o projeto com Maven:

-./mvnw spring-boot:run

-Ou, se tiver Maven instalado:

-mvn spring-boot:run

## 🌐 Acesso

- 📥 Formulário de cadastro: http://localhost:8080/epis.html
- 📦 Listagem JSON de EPIs: http://localhost:8080/epis




