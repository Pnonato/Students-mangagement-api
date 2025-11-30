# 🎓 API para Gerenciamento de Alunos

Este repositório contém uma API desenvolvida como exemplo de um sistema de gerenciamento de estudantes.  
Ela permite cadastrar, editar, listar e excluir alunos, além de implementar autenticação baseada em **JWT (JSON Web Token)**.  
A aplicação utiliza **Node.js**, **Express**, **MongoDB** e diversas bibliotecas voltadas para segurança e organização.

---

## 🧩 Funcionalidades

- **➕ Cadastro de Alunos:** Adiciona novos registros contendo nome, RA e notas.
- **📋 Listagem de Alunos:** Consulta geral ou individual por ID.
- **📈 Média dos Alunos:** Retorna o nome e a média de todos os estudantes cadastrados.
- **✔️ Status de Aprovação:** Indica se cada aluno está aprovado ou reprovado de acordo com a média.
- **📝 Atualização de Dados:** Permite modificar informações de um aluno por ID.
- **➖ Exclusão:** Remove um aluno específico.
- **🔒 Autenticação com JWT:** Proteção de rotas e gerenciamento de acesso.
- **👤 Registro e Login:** Criação de usuários e autenticação no sistema.

---

## 📋 Requisitos

Certifique-se de ter instalado:

- [Node.js](https://nodejs.org/) — Ambiente de execução JavaScript.
- [MongoDB](https://www.mongodb.com/) — Banco de dados utilizado pelo sistema.

---

## 🚀 Tecnologias Utilizadas

- **Node.js** — Backend em JavaScript  
- **Express** — Framework para criação de servidores HTTP  
- **Mongoose** — ODM utilizado para interagir com o MongoDB  
- **JWT (jsonwebtoken)** — Autenticação baseada em token  
- **bcrypt** — Criptografia de senhas  
- **dotenv** — Controle de variáveis de ambiente  
- **Nodemon** — Reload automático durante o desenvolvimento  

---

## 🛠️ Como Executar o Projeto

1. Clone o repositório:

   ```bash
   git clone <URL_DO_REPOSITORIO>
   cd <NOME_DO_PROJETO>
   ```

2. Instale as dependências:

   ```bash
   npm install
   ```

3. Configure as variáveis de ambiente:

   Crie um arquivo `.env` na raiz do projeto e adicione as seguintes variáveis:

   ```env
   PORT=3000 // Por padrão o servidor irá rodar na porta 3000, mesmo que a variável não seja adicionada
   MONGO_URI=mongo_db_url
   JWT_SECRET=sua_chave_secreta
   ```

4. Inicie o servidor de desenvolvimento:

   ```bash
   npm run dev
   ```

5. Acesse a API no endereço: [http://localhost:3000](http://localhost:3000)

---

## 🔀 Rotas da API

### Autenticação
- `POST /register` - Registro de novos usuários.
- `POST /login` - Login e geração de um token JWT.

### Alunos (rotas protegidas com JWT)
- `GET /alunos` - Retorna todos os alunos cadastrados.
- `GET /alunos/:id` - Retorna um aluno específico pelo ID.
- `GET /alunos/medias` - Retorna o nome e a média de todos os alunos.
- `GET /alunos/aprovados` - Retorna os alunos com seus status (aprovado/reprovado).
- `POST /alunos` - Cadastra um novo aluno.
- `PUT /alunos/:id` - Atualiza as informações de um aluno.
- `DELETE /alunos/:id` - Exclui um aluno pelo ID.

---

## ✨ Considerações Finais

Este projeto foi desenvolvido com foco em fornecer um exemplo prático de uma API RESTful com autenticação, protegendo rotas com JWT e gerenciando dados de forma eficiente utilizando o MongoDB.  
Com a implementação de boas práticas e ferramentas modernas, é possível expandir e adaptar o projeto para diferentes cenários do mundo real.
