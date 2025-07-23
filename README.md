# Blog Pessoal - CRUD com NestJS

Este projeto faz parte das atividades práticas do curso **Generation Brasil**, com o objetivo de desenvolver um **CRUD completo para um Blog Pessoal** utilizando o framework **NestJS**.

---

## ✅ Resumo do projeto

O projeto consiste na construção de uma **API RESTful** para gerenciamento de postagens e temas de um blog pessoal. Foram implementados:

- Configuração inicial do projeto com NestJS e TypeORM.
- Conexão com o banco de dados **MySQL** (db_blogpessoal).
- Criação do recurso **Postagem**, incluindo:
  - Entidade `Postagem` mapeando a tabela `tb_postagens`
  - Módulo `PostagemModule`
  - Serviço `PostagemService` com todos os métodos: `findAll`, `findById`, `findByTitulo`, `create`, `update` e `delete`
  - Controlador `PostagemController` expondo as rotas da API
- Criação do recurso **Tema**, incluindo:
  - Entidade `Tema` mapeando a tabela `tb_temas`
  - Módulo `TemaModule`
  - Serviço `TemaService` com os métodos: `findAll`, `findById`, `findByDescricao`, `create`, `update` e `delete`
  - Controlador `TemaController` expondo as rotas da API
- **Relacionamento bidirecional** entre Tema e Postagem:
  - Um Tema pode conter várias Postagens (`@OneToMany`)
  - Uma Postagem pertence a um único Tema (`@ManyToOne`)
- Testes completos via **Insomnia**:
  - Criação e atualização de postagens com vínculo ao tema
  - Busca por título (`GET /postagens/titulo/:titulo`)
  - Busca por descrição do tema (`GET /temas/descricao/:descricao`)
- Versionamento completo do projeto no **GitHub**, seguindo as boas práticas exigidas pela Generation Brasil.

---

## 🚀 Tecnologias utilizadas

- NestJS
- TypeScript
- Node.js
- MySQL
- TypeORM
- Insomnia (testes de API)
- Git e GitHub

---

## 🧪 Funcionalidades da API

### 📌 Rotas de Postagem
- `GET /postagens`
- `GET /postagens/:id`
- `GET /postagens/titulo/:titulo`
- `POST /postagens`
- `PUT /postagens`
- `DELETE /postagens/:id`

### 📌 Rotas de Tema
- `GET /temas`
- `GET /temas/:id`
- `GET /temas/descricao/:descricao`
- `POST /temas`
- `PUT /temas`
- `DELETE /temas/:id`

---

## 🧩 Relacionamento

- `Postagem` → `Tema` → relacionamento **muitos-para-um**
- `Tema` → `Postagem` → relacionamento **um-para-muitos**


---


🧑‍💻 Autora

[Vanessa Targino](https://github.com/VanessaTargino)
>>>>>>> 6740d740693ed25f9275865445b9533c4167a7fb
