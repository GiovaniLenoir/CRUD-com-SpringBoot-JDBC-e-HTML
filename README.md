# 🛡️ Sistema de Controle de EPIs

Este é um sistema simples para **cadastro e listagem de EPIs (Equipamentos de Proteção Individual)**, desenvolvido com **Spring Boot**, **JDBC** e **HTML**. O projeto utiliza **MySQL** como banco de dados e fornece uma interface básica para interações com o sistema.

## 🚀 Funcionalidades

- Cadastrar novos EPIs
- Listar todos os EPIs cadastrados (em JSON)
- Interface HTML simples para entrada de dados

## 🗂 Estrutura do Projeto

```
projeto-epi/
├── pom.xml
├── src/
│   ├── main/
│   │   ├── java/com/exemplo/epi/
│   │   │   ├── Epi.java
│   │   │   ├── EpiController.java
│   │   │   └── EpiRepository.java
│   │   └── resources/
│   │       ├── static/epis.html
│   │       └── application.properties
```

## 🛠 Tecnologias Utilizadas

- Java 17+ (ou compatível com Spring Boot)
- Spring Boot
- Spring JDBC
- MySQL
- HTML/CSS
- Maven

## 📦 Requisitos

- Java JDK instalado
- MySQL Server em execução
- Maven instalado (ou use o wrapper `./mvnw`)

## 🧑‍💻 Como Executar o Projeto

1. **Clone o projeto ou extraia o `.zip`:**

```bash
unzip projeto-epi-completo.zip
cd projeto-epi
```

2. **Configure o banco de dados MySQL:**

Abra o MySQL e execute:

```sql
CREATE DATABASE episdb;
USE episdb;

CREATE TABLE epis (
  id INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(100) NOT NULL,
  validade DATE NOT NULL
);
```

3. **Verifique as configurações em** `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/episdb
spring.datasource.username=root
spring.datasource.password=
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
```

4. **Execute o projeto:**

Com Maven instalado:

```bash
mvn spring-boot:run
```

Ou com o wrapper:

```bash
./mvnw spring-boot:run
```

## 🌐 Acessando o Sistema

- **Cadastro de EPI (HTML):** [http://localhost:8080/epis.html](http://localhost:8080/epis.html)
- **Listagem em JSON:** [http://localhost:8080/epis](http://localhost:8080/epis)

## 📁 Arquivos Importantes

- `Epi.java`: Classe modelo do EPI
- `EpiRepository.java`: Acesso ao banco via JdbcTemplate
- `EpiController.java`: Controlador para rotas HTTP
- `epis.html`: Formulário para cadastrar novos EPIs




