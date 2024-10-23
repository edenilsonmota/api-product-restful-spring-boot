# API RESTful de Produtos

API para gerenciar produtos utilizando **Java 21**, **Spring Boot**, **PostgreSQL** e **Maven**.

## Pré-requisitos

- **Java 21**
- **Maven**
- **PostgreSQL** com um banco de dados `product`

### Configuração do Banco de Dados

crie o banco de dados no PostgreSQL:
```
CREATE DATABASE product;
```

Atualize o arquivo `src/main/resources/application.properties` com suas credenciais:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/product
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
```

## Instalação e Execução

1. Clone o repositório:

    ```bash
    git clone https://github.com/edenilsonmota/api-product-restful-spring-boot.git
    cd api-product-restful-spring-boot
    ```

2. Compile e execute o projeto:

    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

## Endpoints

- **POST** `/api/products`: Cria um produto
    ```json
    { 
      "name": "Mesa", 
      "value": 300.00 
    }
    ```

- **GET** `/api/products`: Lista todos os produtos

- **GET** `/api/products/{id}`: Busca um produto por ID

- **PUT** `/api/products/{id}`: Atualiza um produto

- **DELETE** `/api/products/{id}`: Deleta um produto

## Tecnologias

- Java 21, Spring Boot, PostgreSQL, Maven