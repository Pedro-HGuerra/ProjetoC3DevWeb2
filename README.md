# Projeto C3 com JWT, Docker, Prisma e TypeScript

Este projeto é uma API que permite gerenciar usuários, posts e comentários, utilizando JSON Web Tokens (JWT) para autenticação, Docker para contêinerização, Prisma como ORM, e TypeScript para segurança e eficiência no desenvolvimento.

## Tecnologias Utilizadas

- **TypeScript**: Linguagem de programação utilizada para escrever o código.
- **JWT**: Utilizado para autenticação e autorização de usuários.
- **Docker**: Utilizado para criar e gerenciar contêineres para o desenvolvimento e deploy da aplicação.
- **Prisma**: ORM utilizado para gerenciar e interagir com o banco de dados.

## Pré-requisitos

Certifique-se de ter os seguintes softwares instalados em sua máquina:

- [Node.js](https://nodejs.org/)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)
- [Git](https://git-scm.com/)

## Configuração do Ambiente

1. **Clone o Repositório**

   ```bash
   git clone https://github.com/seu-usuario/ProjetoC3DevWeb2.git
   cd ProjetoC3DevWeb2 
   ```

2. **Instale as Dependências**

   ```bash
   npm install
   ```

3. **Configure as Variáveis de Ambiente**

   Crie um arquivo `.env` na raiz do projeto com o seguinte conteúdo:

   ```plaintext
   DATABASE_URL="file:./dev.db"
   JWT_TOKEN_VALIDATION="SEU_TOKEN_AQUI"
   ```

   - `DATABASE_URL`: URL de conexão com o banco de dados. Neste exemplo, estamos utilizando um banco de dados SQLite armazenado localmente.
   - `JWT_TOKEN_VALIDATION`: Token usado para validar as operações JWT. Substitua `"SEU_TOKEN_AQUI"` por um token seguro de sua escolha.

## Executando a Aplicação com Docker

1. **Construa a Imagem Docker**

   ```bash
   docker-compose build
   ```

2. **Inicie os Contêineres**

   ```bash
   docker-compose up
   ```

   A aplicação estará disponível em `http://localhost:3000`.

## Estrutura do Projeto

- **/src**
  - Contém o código-fonte da API.
- **/prisma**
  - Contém os arquivos de configuração e migrações do Prisma.
- **/docker**
  - Configurações para os contêineres Docker.
- **.env**
  - Arquivo de configuração das variáveis de ambiente.

## Utilização da API

A API possui endpoints para gerenciar usuários, posts e comentários. Aqui está um exemplo básico de como interagir com a API:

### Endpoints

- **Usuários**
  - `POST /api/users`: Cria um novo usuário.
  - `GET /api/users`: Lista todos os usuários.
  - `PATCH /api/users/:id`: Atualiza um usuário.
  - `DELETE /api/users/:id`: Remove um usuário.

- **Posts**
  - `POST /api/post/create`: Cria um novo post.
  - `GET /api/post/getallpost`: Lista todos os posts.
  - `GET /api/post/getPostByUserId/:id`: Retorna detalhes de um post específico.
  - `PATCH /api/post/update/:id`: Atualiza um post.
  - `DELETE /api/post/delete/:id`: Remove um post.

- **Comentários**
  - `POST /api/comment/create`: Cria um novo comentário.
  - `GET /api/comment/getallcomment`: Lista todos os comentários.
  - `GET /api/comment/getcommentByUserId/:id`: Retorna detalhes de um comentário específico.
  - `PATCH /api/comment/update/:id`: Atualiza um comentário.
  - `DELETE /api/comment/delete/:id`: Remove um comentário.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

## Contato

- Autor: [Pedro Henrique Guerra](https://github.com/Pedro-HGuerra)
- Email: pedro.hguerra11.com

---
