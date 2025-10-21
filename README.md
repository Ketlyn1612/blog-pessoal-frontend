Blog Pessoal (Java + Spring Boot)

Projeto desenvolvido durante o bootcamp da Generation Brasil, utilizando Spring Boot para o back-end. É uma API REST para gerenciamento de posts de blog, usuários e comentários.

💻 Tecnologias usadas

Java 17

Spring Boot

Spring Data JPA

MySQL

Maven

Swagger / Postman (para documentação e testes)

🗂 Estrutura da API
Endpoints principais
Método	Rota	Descrição
GET	/usuarios	Lista todos os usuários
GET	/usuarios/{id}	Busca usuário por ID
POST	/usuarios	Cadastra novo usuário
PUT	/usuarios	Atualiza usuário existente
DELETE	/usuarios/{id}	Deleta usuário
GET	/postagens	Lista todas as postagens
GET	/postagens/{id}	Busca postagem por ID
POST	/postagens	Cria nova postagem
PUT	/postagens	Atualiza postagem existente
DELETE	/postagens/{id}	Deleta postagem
Entidades principais

Usuario

id (Long)

nome (String)

email (String)

senha (String)

Postagem

id (Long)

titulo (String)

texto (String)

data (LocalDateTime)

usuario (Usuario)

Comentario (opcional)

id (Long)

texto (String)

data (LocalDateTime)

postagem (Postagem)

usuario (Usuario)

🗄 Banco de Dados

MySQL

Exemplo de script de criação de banco:

CREATE DATABASE blog_pessoal;


Configuração no application.properties:

spring.datasource.url=jdbc:mysql://localhost:3306/blog_pessoal
spring.datasource.username=root
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

📷 Testes e documentação

Swagger: disponível em http://localhost:8080/swagger-ui.html

Postman: coleção de testes para todos os endpoints (opcional: link para a coleção)




🚀 Como rodar o projeto

Clonar o repositório:

git clone https://github.com/seu-usuario/blog-pessoal.git


Configurar o banco de dados MySQL.

Rodar a aplicação:

mvn spring-boot:run


Acessar os endpoints via Swagger ou Postman.
