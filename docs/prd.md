# 📄 Product Requirements Document (PRD) – ContraTerra

## 1. 🧭 Visão Geral e Objetivo

O **ContraTerra** é uma aplicação web que permite aos usuários acompanhar notícias e compartilhar opiniões sobre conteúdos como filmes, séries, games e entretenimento em geral.

A aplicação tem como foco:

* Exibição de **notícias atualizadas**
* Interação entre usuários (comentários e avaliações)
* Interface simples, responsiva e intuitiva

O backend será simulado utilizando **JSON Server**, permitindo operações básicas de leitura e escrita de dados.

---

## 2. 👥 Atores do Sistema

* **Visitante**

  * Acessa a aplicação sem login
  * Visualiza notícias e conteúdos

* **Usuário**

  * Possui conta e está autenticado
  * Pode comentar e avaliar conteúdos

* **Sistema (API Fake)**

  * Responsável por armazenar e retornar dados (notícias, usuários, comentários, avaliações)

---

## 3. 🧩 Histórias de Usuário e Escopo (MVP)

### 📰 Épico 1: Visualização de Conteúdo

* **US01 - Listar Notícias**
  Como um visitante, quero visualizar uma lista de notícias para acompanhar conteúdos de cultura pop.

  * *Critérios de Aceitação:*

    * Exibir título, imagem e resumo
    * Layout em cards responsivos

* **US02 - Visualizar Detalhes da Notícia**
  Como um usuário, quero abrir uma notícia para ver seu conteúdo completo.

  * *Critérios de Aceitação:*

    * Exibir título, imagem, conteúdo completo e data

---

### 👤 Épico 2: Autenticação

* **US03 - Cadastro de Usuário**
  Como um visitante, quero criar uma conta informando nome, email e senha.

  * *Critérios de Aceitação:*

    * Todos os campos obrigatórios
    * Validação de email
    * Dados armazenados na API fake

* **US04 - Login**
  Como um usuário, quero acessar o sistema com email e senha.

  * *Critérios de Aceitação:*

    * Validação de credenciais
    * Sessão salva no localStorage

---

### 💬 Épico 3: Comentários

* **US05 - Comentar em Notícias**
  Como um usuário logado, quero comentar em uma notícia.

  * *Critérios de Aceitação:*

    * Campo de texto obrigatório
    * Comentário vinculado à notícia
    * Exibição imediata após envio

* **US06 - Visualizar Comentários**
  Como um usuário, quero ver comentários de outros usuários.

  * *Critérios de Aceitação:*

    * Lista com nome do usuário e conteúdo
    * Ordenação por data

---

### ⭐ Épico 4: Avaliações

* **US07 - Avaliar Conteúdo**
  Como um usuário, quero dar uma nota para um conteúdo (ex: filme/série).

  * *Critérios de Aceitação:*

    * Nota de 0 a 5
    * Armazenamento na API

* **US08 - Visualizar Avaliações**
  Como um usuário, quero ver a média de avaliações.

  * *Critérios de Aceitação:*

    * Exibir média das notas
    * Atualização dinâmica

---

### 🔎 Épico 5: Busca e Filtro

* **US09 - Buscar Conteúdo**
  Como um usuário, quero buscar notícias por título.

  * *Critérios de Aceitação:*

    * Campo de busca funcional
    * Filtragem em tempo real ou por botão

---

## 4. 🧱 Regras de Negócio

* Apenas usuários logados podem:

  * comentar
  * avaliar

* Campos obrigatórios:

  * cadastro
  * login
  * comentários

* Avaliações devem estar entre **0 e 5**

* Cada comentário deve estar vinculado a:

  * um usuário
  * uma notícia

---

## 5. 🛠️ Requisitos Técnicos (Simplificado)

### Frontend

* HTML5
* CSS3 (com Framework CSS como Bootstrap ou Tailwind)
* JavaScript (com uso opcional de jQuery)

### Backend (Simulado)

* JSON Server (API Fake)

### Armazenamento

* localStorage para sessão do usuário

---

## 6. 🎨 Requisitos de Interface (UI)

* Layout responsivo (mobile e desktop)
* Uso de:

  * cards para notícias
  * navbar
  * botões padronizados
* Design consistente (cores, tipografia)

---

## 7. 🔗 Integração com API

A aplicação deve consumir endpoints como:

* `/news` → listar notícias
* `/users` → cadastro/login
* `/comments` → comentários
* `/reviews` → avaliações

Operações:

* GET (listar dados)
* POST (criar dados)

---

## 8. 🚀 Fora do Escopo (para manter simples)

* Sistema real de autenticação (JWT, etc.)
* Upload de imagens
* Sistema de seguidores
* Chat em tempo real
