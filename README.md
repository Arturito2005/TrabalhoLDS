# TrabalhoLDS

## English

## Acronym List
| Acronym | Description |
| :--- | :--- |
| LDS | Software Development Laboratory |
| CMU | Mobile and Ubiquitous Computing |

### 📌 Introduction
This project consists of an amateur football match management platform, designed to connect players and promote healthy competition. The system allows users to create their own teams and challenge other groups, facilitating the organization of both casual and competitive matches.

**Project Context:**
Developed within the scope of the **LDS** (Software Development Laboratory) and **CMU** (Mobile and Ubiquitous Computing) curricular units, focusing on the integration between a robust API and client interfaces.

**Solution Architecture:**
The ecosystem is composed of three main pillars:
* **Backend:** A central RESTful API developed in .NET.
* **Mobile (Android):** The main application (core focus of the CMU course), delivering the complete user experience.
* **Web:** A supporting web interface.

---

### 👥 User Roles
The system defines three distinct access levels:

* **Team Administrator:** Responsible for roster management (join requests and members) and match organization. Each team allows a maximum of 4 administrators.
* **Team Member:** A player linked to a team. Has read-only access to team data and the match schedule.
* **Free Agent:** A user without a team. Can browse profiles and send join requests to teams with open spots.

---

### 🚀 Key Features

**1. Team Management**
* **Full CRUD:** Creation, editing, viewing, and deletion of teams.
* **Team Chat:** Chat available for each match, accessible only to the administrators of both opposing teams.
* **Roster Management:** Tools for administrators to remove members or manage hierarchies (promoting/demoting admins).
* **Recruitment System:** Management of join requests (accepting, rejecting, or viewing applications from free agents).

**2. Match Management**
* **Casual Matches (Challenge Mode):** Complete challenge cycle between teams. Includes a negotiation flow (sending proposals and counter-proposals for time/location), scheduling, and state management (start, finish, postpone, or cancel match).
* **Competitive Matchmaking:** Automatic system that pairs teams for official matches based on four criteria: Rank, Points, Average Age, and Location.

**3. Social & Gamification**
* **Leaderboard:** Global ranking table displaying the Top 100 teams, sorted by rank and points.
* **User Profile:** Personal data management and ability to view other players' profiles.
* **Join Request Management:** Area where free agents can manage received invitations and send requests to teams.
* **Notification Center:** Real-time alerts regarding relevant events (invites, roster changes, match updates, etc.).

---

### 📡 External Services & APIs
* **OpenStreetMap:** Geolocation engine and interactive map visualization. Also used for *geocoding* services (validating and converting addresses into coordinates).
* **Cloudinary:** *Cloud storage* solution for media management. Responsible for hosting and optimizing player profile images and team badges.

---

### 🛠️ Tech Stack & Tools

The project architecture is distributed across three main layers, supported by cloud services and containerization.

#### 🔙 Backend (.NET)
The core of the system, responsible for business logic and data processing.
* **C# & .NET:** Main framework for RESTful API development.
* **SignalR:** Used for real-time communication via *WebSockets*. Essential for **Matchmaking** Hubs, allowing instant start, state management, and completion of competitive matches.
* **SQL Server:** Relational database for structured data persistence.
* **NUnit:** Framework used for unit testing, ensuring code reliability.
* **DocFx:** Tool for generating static technical documentation from .NET source code.
* **Swagger:** Interactive interface for documentation and testing of API *endpoints*.

#### 📱 Mobile (Native Android)
The primary interface for the end-user.
* **Kotlin:** Modern language used for native Android development.
* **Retrofit:** *Type-safe* HTTP client for communication and consumption of the REST API.
* **Dagger Hilt:** Dependency Injection (DI) framework, facilitating component management and testability.
* **Dokka:** Documentation engine for Kotlin code (equivalent to Javadoc/DocFx).

#### 🌐 Web Frontend
Administrative and support interface.
* **Angular:** Framework used for building SPAs (*Single Page Applications*), utilizing **TypeScript**, **HTML5**, and **CSS3**.
* **Cypress:** Framework for executing End-to-End (E2E) tests on the web system.

#### ☁️ Cloud & DevOps
Transversal services and infrastructure.
* **Firebase Realtime Database:** Used to manage chat rooms and persist dynamic user information.
* **Firebase Cloud Messaging (FCM):** *Push* notification system. Ensures the user receives alerts (invites, games) whether the app is in the foreground or background.
* **Docker:** Used for application containerization, ensuring consistency between development and production environments.
---

### 🔗 Links
In this repository, we provide the project report as well as links to our backend and frontend repositories.

**Access Links:**
- **Backend:** https://github.com/Btx69-jpg/Backend-LDS
- **Mobile Frontend:** https://github.com/Btx69-jpg/FrontendMobile-FutebolAmador
- **Web Frontend:** https://github.com/Btx69-jpg/FrontendWeb-FutebolAmador

## Português

## Lista de Siglas
| Sigla | Descrição |
| -------- | -------- | 
| LDS  | Laboratório de Desenvolvimento de Software  | 
| CMU  | Computação Móvel e Oblíqua  |

### 📌 Introdução
Este projeto consiste numa plataforma de gestão de partidas de futebol amador, desenvolvida para conectar jogadores e promover a competitividade saudável. O sistema permite que utilizadores criem as suas próprias equipas e desafiem outros grupos, facilitando a organização de jogos casuais ou competitivos.

Contexto do Projeto: Desenvolvido no âmbito das unidades curriculares de LDS e CMU, com foco na integração entre uma API robusta e interfaces cliente.

Arquitetura da Solução: O ecossistema é composto por três pilares desenvolvidos em .NET:
* **Backend**: Uma API RESTful central.
* **Mobile (Android)**: A aplicação principal (foco da UC de CMU), contendo a experiência completa do utilizador.
* **Web**: Uma interface web de suporte.

---
### 👥 Tipos de Utilizadors
O sistema define três níveis de acesso distintos:

* **Administrador de Equipa:** Responsável pela gestão do plantel (pedidos de adesão e membros) e organização de partidas. Cada equipa permite um máximo de 4 administradores.
* **Membro de Equipa:** Jogador vinculado a uma equipa. Possui acesso de consulta aos dados da equipa e ao calendário de jogos.
* **Jogador Livre:** Utilizador sem equipa. Pode consultar perfis e enviar pedidos de adesão a equipas com vagas disponíveis.

### 🚀 Principais Funcionalidades

**1. Gestão de Equipas**
* **CRUD Completo:** Criação, edição, consulta e eliminação de equipas.
* **Chat de Equipas** Chat disponivel para cada partida da equipa disponível apenas para os administradores das duas equipas.
* **Gestão de Plantel:** Ferramentas para administradores removerem membros ou gerirem hierarquias (promoção/despromoção de admins).
* **Sistema de Recrutamento:** Gestão de pedidos de adesão (aceitar, rejeitar ou consultar candidaturas de jogadores livres).

**2. Gestão de Partidas**
* **Partidas Casuais (Modo Desafio):** Ciclo completo de desafio entre equipas. Inclui fluxo de negociação (envio de propostas e contra-propostas de horário/local), agendamento, e gestão de estado (iniciar, finalizar, adiar ou cancelar jogo).
* **Matchmaking Competitivo:** Sistema automático que emparelha equipas para jogos oficiais baseando-se em quatro critérios: Rank, Pontuação, Idade Média e Localização.

**3. Social e Gamificação**
* **Leaderboard:** Tabela de classificação global exibindo o Top 100 equipas, ordenadas por rank e pontos.
* **Perfil de Utilizador:** Gestão de dados pessoais e consulta de perfis de outros jogadores.
* **Gestão de pedidos adesão**: Onde cada jogador sem equipa poderá gerir os pedidos recebidos para aderiar a equipas e mandar pedidos às mesmas
* **Centro de Notificações:** Alertas em tempo real sobre eventos relevantes (convites, alterações no plantel, atualizações de jogos, etc.).
  
---
### 📡 APIs Utilizadas
* **OpenStreetMap:** Motor de geolocalização e visualização de mapas interativos. Utilizado também para serviços de *geocoding* (validação e conversão de moradas em coordenadas).
* **Cloudinary:** Solução de *cloud storage* para gestão de media. Responsável pelo alojamento e otimização das imagens de perfil dos jogadores e emblemas das equipas.

---
### 🛠️ Tech Stack e Ferramentas

A arquitetura do projeto é distribuída em três camadas principais, suportadas por serviços cloud e containerização.

#### 🔙 Backend (.NET)
O núcleo do sistema, responsável pela lógica de negócio e processamento de dados.
* **C# & .NET:** Framework principal para o desenvolvimento da API RESTful.
* **SignalR:** Utilizado para comunicação em tempo real via *WebSockets*. Fundamental para os Hubs de **Matchmaking**, permitindo iniciar, gerir estados e finalizar partidas competitivas instantaneamente.
* **SQL Server:** Base de dados relacional para persistência de dados estruturados.
* **NUnit:** Framework utilizado para testes unitários, garantindo a fiabilidade do código.
* **DocFx:** Ferramenta para gerar documentação técnica estática a partir do código fonte .NET.
* **Swagger:** Interface interativa para documentação e teste dos *endpoints* da API.

#### 📱 Mobile (Android Nativo)
A interface principal para o utilizador final.
* **Kotlin:** Linguagem moderna utilizada para o desenvolvimento nativo Android.
* **Retrofit:** Cliente HTTP *type-safe* para comunicação e consumo da API REST.
* **Dagger Hilt:** Framework para Injeção de Dependências (DI), facilitando a gestão de componentes e a testabilidade.
* **Dokka:** Motor de documentação para código Kotlin (equivalente ao Javadoc/DocFx).

#### 🌐 Frontend Web
Interface administrativa e de suporte.
* **Angular:** Framework utilizado para a construção das SPA (*Single Page Applications*), utilizando **TypeScript**, **HTML5** e **CSS3**.
* **Cypress:** Framework para execução de testes "End-to-End" (E2E) no sistema web.

#### ☁️ Cloud & DevOps
Serviços transversais e infraestrutura.
* **Firebase Realtime Database:** Utilizado para gerir as salas de chat (Rooms) e persistir informações dinâmicas de utilizadores.
* **Firebase Cloud Messaging (FCM):** Sistema de notificações *Push*. Garante que o utilizador recebe alertas (convites, jogos) tanto com a app em primeiro plano (*foreground*) como fechada (*background*).
* **Docker:** Utilizado para containerização da aplicação, garantindo consistência entre ambientes de desenvolvimento e produção.

---
### 🔗 Links
Neste repositorio disponibilizamos o relatorio do trabalho e também os links para os repositorios com o nosso backend e frontend.
Links para aceder ao Backend ou Frontend:
- **Backend**: https://github.com/Btx69-jpg/Backend-LDS
- **Frontend Mobile**: https://github.com/Btx69-jpg/FrontendMobile-FutebolAmador
- **Frontend Web**: https://github.com/Btx69-jpg/FrontendWeb-FutebolAmador
