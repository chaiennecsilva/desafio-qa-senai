# 📚 Projeto - Sistema de Cadastro e Login de Usuários

## 📋 Descrição

Este projeto foi desenvolvido para o processo seletivo **00925/2025 - Analista de Qualidade Software - Júnior - SENAI/SC - Soluções Digitais**.
O objetivo é criar uma aplicação web simples, dividida em **backend** e **frontend**, utilizando banco de dados **PostgreSQL**, conforme as instruções fornecidas.

A aplicação permite:

* Cadastro de usuários.
* Login de usuários.
* Listagem de usuários cadastrados.

---

## 🚀 Tecnologias utilizadas

* **Backend:**

  * Node.js
  * Express
  * Cors
  * PostgreSQL (`pg`)
  * Dotenv

* **Frontend:**

  * HTML5
  * Javascript puro (fetch API)

* **Banco de Dados:**

  * PostgreSQL

* **Versionamento:**

  * Git

---

## ⚙️ Como executar o projeto

### 1. Clonar o repositório

```bash
git clone <URL_DO_REPOSITÓRIO>
cd nome-do-projeto
```

### 2. Configurar o Banco de Dados

* Criar um banco no PostgreSQL.
* Executar o script abaixo para criar a tabela de usuários:

```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  password VARCHAR(100) NOT NULL
);
```

### 3. Configurar o ambiente

Criar um arquivo `.env` na pasta `backend` com o conteúdo:

```
PORT=3000
DB_HOST=localhost
DB_USER=seu_usuario
DB_PASSWORD=sua_senha
DB_DATABASE=nome_do_banco
DB_PORT=5432
```

### 4. Instalar dependências do backend

```bash
cd backend
npm install
```

### 5. Executar o backend

```bash
node server.js
```

O backend estará rodando em: `http://localhost:3000`

### 6. Executar o frontend

Basta abrir o arquivo `frontend/index.html` em um navegador web.

---

## 📄 Funcionalidades implementadas

* Cadastro de novos usuários.
* Login de usuários.
* Validação básica de login.
* Listagem de usuários cadastrados após login.

---

## 🧪 Plano de Testes Executados

Foram realizados testes manuais básicos para garantir o funcionamento das principais funcionalidades da aplicação:

* **Cadastro de novo usuário:**

  * Preenchimento correto de todos os campos (Nome, E-mail, Senha).
  * Tentativa de cadastro com campos em branco (esperado erro).
  * Tentativa de cadastro com e-mail já registrado (esperado erro de duplicidade).

* **Login de usuário:**

  * Login com credenciais corretas (esperado sucesso).
  * Login com e-mail ou senha incorretos (esperado erro).

* **Listagem de usuários:**

  * Verificação da listagem de todos os usuários cadastrados após login.

**Resultado esperado:**
Em todos os cenários testados, o sistema respondeu conforme esperado, garantindo a integridade das operações básicas.

---

## 🔧 Melhorias sugeridas

Caso a aplicação fosse evoluída, as seguintes melhorias poderiam ser aplicadas:

* **Hash de senhas:**
  Implementar criptografia de senhas utilizando `bcrypt` para aumentar a segurança dos dados armazenados.

* **Validação de formulários:**
  Adicionar validações front-end para impedir o envio de formulários com campos em branco.

* **Testes automatizados:**
  Criar testes unitários e de integração utilizando ferramentas como `jest`, `supertest` ou `mocha`.

* **Tratamento de erros:**
  Melhorar o tratamento de exceções no backend para fornecer mensagens de erro mais detalhadas ao usuário.

* **Página de login protegida:**
  Após login, proteger as rotas para acesso apenas de usuários autenticados, usando JWT (JSON Web Token).

* **Paginação da listagem de usuários:**
  Adicionar paginação na tela de listagem para melhor desempenho e usabilidade.

---

## 📌 Observação Final

Este projeto foi desenvolvido de forma simples, com foco em entregar uma aplicação funcional, organizada e com boa documentação, alinhada aos princípios de qualidade de software.
O objetivo principal foi garantir a entrega com código limpo, funcionalidades testadas e uma visão de possíveis evoluções futuras.

---

## ✍️ Desenvolvido por

**\[Chaienne Silva]** — Maio/2025.

---
