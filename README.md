# performaceVendas
📊 Dashboard full-stack de Performance de Vendas com gamificação e cálculo automatizado de comissões (Gatilhos). Desenvolvido com Spring Boot (Java), React, PostgreSQL e Docker.
# 🚀 Performance System - Dashboard de Vendas

![Status](https://img.shields.io/badge/Status-Em%20Desenvolvimento-green)
![Java](https://img.shields.io/badge/Spring%20Boot-3.2-brightgreen)
![React](https://img.shields.io/badge/React-Vite-blue)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED)

## 📌 Sobre o Projeto
O **Performance Vendas** é uma aplicação Full-Stack desenvolvida para o gerenciamento e visualização de indicadores de performance de equipes de vendas. O sistema integra um painel gamificado (Ranking) com o cálculo automatizado de metas e comissões com base em gatilhos de vendas.

O projeto foi estruturado com foco em **Arquitetura Escalável**, separando claramente as responsabilidades entre Frontend, Backend e Banco de Dados, utilizando contêineres Docker para facilitar a reprodutibilidade do ambiente.

## 🎯 Funcionalidades
- **Dashboard em Tempo Real:** Visualização do Total de Vendas, Meta Projetada e o valor restante para atingir o próximo nível de comissão.
- **Métricas de Atendimento:** Cálculo automático da taxa de conversão (Atendimentos vs. Vendas Fechadas).
- **Ranking Gamificado:** Listagem automática dos Top 5 Vendedores (Desafio Semanal), destacando a liderança.
- **Motor de Regras de Negócio (Gatilhos):** O backend calcula a comissão dinamicamente:
  - Vendas < R$ 1.000,00: Sem comissão (Ativação mínima)
  - Vendas > R$ 2.000,00: 25%
  - Vendas > R$ 2.200,00: 40%
  - Vendas > R$ 2.500,00: 60%
  - Vendas > R$ 2.500,00 (Teto): 80%
- **Gestão de Acesso:** Tela de login para controle de permissões (Administradores lançam dados, usuários visualizam).

## 🛠️ Tecnologias Utilizadas
- **Frontend:** React (Vite), Tailwind CSS, Axios.
- **Backend:** Java 21, Spring Boot (Web, Data JPA, Security).
- **Banco de Dados:** PostgreSQL 15.
- **Infraestrutura:** Docker e Docker Compose (para orquestração do Banco e pgAdmin).

## 🚀 Como Executar o Projeto Localmente

### Pré-requisitos
- [Docker Desktop](https://www.docker.com/products/docker-desktop)
- [Node.js](https://nodejs.org/) (versão 18+)
- [Java JDK](https://adoptium.net/) (versão 21+)

### Passo 1: Subir o Banco de Dados
Na raiz do projeto, execute o Docker Compose para iniciar o PostgreSQL:
```bash
docker compose up -d

### Passo 2: Iniciar o Backend (Spring Boot)
Abra a pasta do backend na sua IDE (IntelliJ, Eclipse ou VS Code) e rode a classe principal Application.java. A API estará disponível em http://localhost:8080.

### Passo 3: Iniciar o Frontend (React)
Acesse a pasta do frontend via terminal e rode:

cd frontend
npm install
npm run dev

Acesse a aplicação no navegador em http://localhost:5173.
