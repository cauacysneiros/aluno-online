Explicação do Projeto

O projeto Aluno Online API é uma aplicação backend desenvolvida com Spring Boot que tem como objetivo gerenciar dados de alunos e professores.
A API permite realizar operações completas de CRUD (Create, Read, Update, Delete), possibilitando o cadastro, consulta, atualização e remoção de informações no banco de dados.
O sistema foi desenvolvido com foco em simular um ambiente acadêmico simples, onde é possível armazenar dados como nome, e-mail e CPF de alunos e professores.
A aplicação expõe endpoints REST que podem ser consumidos por ferramentas como Insomnia ou Postman.

Detalhamento do Código
O projeto foi dividido em camadas para melhor organização e manutenção do código:

 Controller
Responsável por receber as requisições HTTP e retornar as respostas.
Exemplo:
- AlunoController
- ProfessorController

Essas classes utilizam anotações como:
- @RestController
- @RequestMapping
- @GetMapping, @PostMapping, @PutMapping, @DeleteMapping

Service
Contém a lógica de negócio da aplicação.
Exemplo:
- AlunoService
- ProfessorService

Nessa camada são feitas operações como:
- salvar dados
- buscar registros
- atualizar informações
- deletar dados

Repository
Responsável pelo acesso ao banco de dados utilizando Spring Data JPA.
Exemplo:
- AlunoRepository
- ProfessorRepository

Essas interfaces estendem JpaRepository, permitindo operações prontas como:
- save()
- findAll()
- findById()
- deleteById()

Model (Entity)
Representa as entidades do banco de dados.
Exemplo:
- Aluno
- Professor

As classes utilizam anotações como:
- @Entity
- @Table
- @Id
- @GeneratedValue

Além disso, foi utilizado o Lombok para reduzir código repetitivo com anotações como:
- @Data
- @NoArgsConstructor
- @AllArgsConstructor

Descrição da Arquitetura

O projeto utiliza a arquitetura em camadas (Layered Architecture), muito comum em aplicações Spring Boot.
Essa arquitetura é composta por:

- Controller (Camada de Apresentação)
Responsável por lidar com as requisições HTTP e respostas da API.

- Service (Camada de Negócio)
Responsável por conter as regras de negócio e processar os dados antes de enviá-los ao banco.

- Repository (Camada de Persistência)
Responsável pela comunicação com o banco de dados utilizando JPA.

- Model (Camada de Dados)
Responsável por representar as entidades que serão armazenadas no banco de dados.

Essa separação garante:
- melhor organização do código
- facilidade de manutenção
- reutilização de componentes
- maior escalabilidade do sistema
