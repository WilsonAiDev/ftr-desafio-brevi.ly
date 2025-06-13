# Brevi.ly - URL Shortener API

<p align="center">
<img alt="TypeScript" src="https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white"/>
<img alt="Fastify" src="https://img.shields.io/badge/fastify-%23000000.svg?style=for-the-badge&logo=fastify&logoColor=white"/>
<img alt="PostgreSQL" src="https://img.shields.io/badge/postgresql-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white"/>
<img alt="Drizzle ORM" src="https://img.shields.io/badge/drizzle-%23C5F74F.svg?style=for-the-badge&logo=drizzle&logoColor=black"/>
<img alt="Docker" src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white"/>
</p>

## 📖 Sobre o Projeto

Este projeto é um desafio de back-end proposto no curso de Pós Graduação em tecnologia **Tech Developer 360** da **FTR (Faculdade Tecnologia Rocketseat)**.

O objetivo é construir uma API RESTful para um serviço de encurtamento de URLs, seguindo os requisitos e a stack de tecnologia especificados. A aplicação permitirá criar, gerenciar, redirecionar e obter métricas de links encurtados.

## ✅ Funcionalidades e Requisitos

A lista abaixo representa as funcionalidades e regras de negócio que devem ser implementadas:

⚠️ **Atenção**: Para esse desafio é esperado a utilização do banco de dados PostgreSQL.

- [ ] Deve ser possível criar um link
- [ ] Não deve ser possível criar um link com URL encurtada mal formatada
- [ ] Não deve ser possível criar um link com URL encurtada já existente
- [ ] Deve ser possível deletar um link
- [ ] Deve ser possível obter a URL original por meio de uma URL encurtada
- [ ] Deve ser possível listar todas as URL's cadastradas
- [ ] Deve ser possível incrementar a quantidade de acessos de um link
- [ ] Deve ser possível exportar os links criados em um CSV
- [ ] Deve ser possível acessar o CSV por meio de uma CDN (Amazon S3, Cloudflare R2, etc)
- [ ] Deve ser gerado um nome aleatório e único para o arquivo
- [ ] Deve ser possível realizar a listagem de forma performática
- [ ] O CSV deve ter campos como: URL original, URL encurtada, contagem de acessos e data de criação

## 🚀 Stack de Tecnologia

Este projeto foi desenvolvido utilizando a seguinte stack de tecnologia:

- **TypeScript**: Linguagem principal do projeto, garantindo tipagem estática e segurança ao código JavaScript.
- **Fastify**: Framework web de alta performance para a construção da API RESTful, escolhido por sua velocidade e baixo overhead.
- **PostgreSQL**: Banco de dados relacional robusto e confiável, utilizado para o armazenamento persistente dos dados da aplicação.
- **Drizzle ORM**: ORM (Object-Relational Mapper) moderno e type-safe para a comunicação segura e intuitiva com o banco de dados PostgreSQL.
- **Docker**: Plataforma de containerização utilizada para criar um ambiente de desenvolvimento e produção consistente e isolado.
- **Cloudflare R2**: Serviço de armazenamento de objetos (compatível com S3) utilizado como CDN para hospedar os arquivos CSV exportados.

## ⚙️ Como Executar o Projeto

### Pré-requisitos

Antes de começar, você vai precisar ter instalado em sua máquina as seguintes ferramentas:

- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org/en/)
- [Docker](https://www.docker.com/) e Docker Compose
- Um gerenciador de pacotes de sua preferência (NPM, Yarn ou PNPM)

### 1. Clonando o Repositório

```bash
git clone https://github.com/seu-usuario/ftr-desafio-brevi.ly.git
cd ftr-desafio-brevi.ly
```

### 2. Instalando as Dependências

```bash
npm install
# ou
yarn install
# ou
pnpm install
```

### 3. Configurando as Variáveis de Ambiente

Copie o arquivo de exemplo `.env.example` para um novo arquivo chamado `.env` e preencha com suas credenciais.

```bash
cp .env.example .env
```

O arquivo `.env` deverá ter a seguinte estrutura:

```env
PORT=3333
DATABASE_URL="postgresql://docker:docker@localhost:5432/shortlinks?schema=public"

# Variáveis para a CDN (Cloudflare R2)
CLOUDFLARE_ACCOUNT_ID=""
CLOUDFLARE_ACCESS_KEY_ID=""
CLOUDFLARE_SECRET_ACCESS_KEY=""
CLOUDFLARE_BUCKET=""
CLOUDFLARE_PUBLIC_URL=""
```

### 4. Subindo o Banco de Dados com Docker

Com o Docker em execução, utilize o Docker Compose para iniciar o container do PostgreSQL:

```bash
docker-compose up -d
```

### 5. Executando as Migrations

Execute o script para criar as tabelas no banco de dados, conforme definido pelo Drizzle ORM:

```bash
npm run db:migrate
```

### 6. Iniciando o Servidor

Agora, inicie o servidor de desenvolvimento:

```bash
npm run dev
```

O servidor estará rodando em `http://localhost:3333` (ou na porta que você definiu no arquivo `.env`).

## 🐳 Usando com Docker

Para construir e executar a aplicação via Docker, siga os passos:

1. **Construa a imagem Docker:**
   ```bash
   docker build -t brevi-ly-api .
   ```

2. **Execute o container:**
   ```bash
   # Certifique-se de que seu arquivo .env está preenchido
   docker run --env-file .env -p 3333:3333 brevi-ly-api
   ```

## 📁 Estrutura do Projeto

```
ftr-desafio-brevi.ly/
├── server/          # API Back-end
├── web/             # Interface Web (opcional)
├── README.md
└── .gitignore
```

---

Feito com ♥ para o desafio **Tech Developer 360** da **FTR**.
