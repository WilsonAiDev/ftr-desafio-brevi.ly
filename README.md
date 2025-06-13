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

## ⚙️ Pré-requisitos

Para rodar o projeto é necessário ter instalado em sua máquina as seguintes ferramentas:

- [Git](https://git-scm.com)
- [Node.js](https://nodejs.org/en/)
- [Docker](https://www.docker.com/) e Docker Compose
- Gerenciador de pacotes de sua preferência, projeto utiliza o PNPM.

---

Feito com ♥ por Wilson Oliveira
