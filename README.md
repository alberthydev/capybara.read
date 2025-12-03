# Capybara.read

![Project Status](https://img.shields.io/badge/Status-In%20Development-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

> **Nota:** Este projeto está atualmente em desenvolvimento ativo. A arquitetura e as funcionalidades estão sendo implementadas conforme o roadmap abaixo.

## Sobre o Projeto

O **Capybara.read** é uma plataforma web desenvolvida para gerenciar clubes do livro, inspirada na necessidade de organizar leituras conjuntas, reviews e recomendações. 

O objetivo principal é criar um ambiente onde membros de um clube (como o *Clube do Livro Mágico dos Felinos e das Capivaras*) possam votar no livro do mês, registrar seu progresso de leitura e receber recomendações personalizadas baseadas em seus gostos literários.

Este projeto também serve como meu **Portfolio Principal** para demonstrar competências em desenvolvimento Full Stack, arquitetura de software e integração de APIs.

## Tech Stack

O projeto utiliza uma arquitetura moderna focada em performance e escalabilidade:

### Front-end
* ![Next JS](https://img.shields.io/badge/Next-black?style=flat-square&logo=next.js&logoColor=white) **Next.js**: Framework React para renderização e rotas.
* ![React](https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB) **React**: Biblioteca para construção de interfaces.
* ![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white) **Tailwind CSS**: Estilização utilitária e responsiva.

### Back-end & Dados
* ![Express.js](https://img.shields.io/badge/Express.js-404D59?style=flat-square) **Express.js**: Servidor API RESTful para lógica de negócios complexa.
* ![Prisma](https://img.shields.io/badge/Prisma-3982CE?style=flat-square&logo=Prisma&logoColor=white) **Prisma ORM**: Gerenciamento de banco de dados e tipagem segura.
* ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=flat-square&logo=postgresql&logoColor=white) **PostgreSQL** (ou SQLite para dev): Banco de dados relacional.

## Funcionalidades Planejadas

- [ ] **Autenticação de Usuários**: Login e cadastro de membros do clube.
- [ ] **Gestão do Livro do Mês**: Votação e definição da leitura atual.
- [ ] **Integração com API Externa**: Busca automática de metadados de livros (Google Books API / Open Library).
- [ ] **Sistema de Reviews**: Avaliação e comentários sobre as leituras.
- [ ] **Algoritmo de Recomendação**: Sugestão de livros baseada no histórico de reviews e gêneros favoritos do usuário.
- [ ] **Dashboard de Leitura**: Visualização de progresso e estatísticas do clube.

## Arquitetura (Draft)

A aplicação segue o padrão MVC (Model-View-Controller) adaptado para a stack Next+Express.

```mermaid
graph TD
    A["Client (Browser)"] -->|HTTP Request| B("Next.js Frontend")
    B -->|API Calls| C{"Express Backend API"}
    C -->|ORM| D["Prisma Client"]
    D -->|Query| E[("Database")]
    C -->|Fetch Info| F["External Book API"]
