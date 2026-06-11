# 🛒 ShopEase 🛍️

> [!NOTE]
> Plataforma B2C de e-commerce para venda de produtos eletrônicos, com catálogo inteligente, carrinho de compras, checkout integrado ao Stripe e painel administrativo completo.

<table>
  <tr>
    <td width="800px">
      <div align="justify">
        O <b>ShopEase</b> é uma plataforma de e-commerce moderna voltada ao segmento de eletrônicos, desenvolvida com foco em <i>experiência do usuário</i>, <i>segurança</i> e <i>escalabilidade</i>. O sistema permite que clientes naveguem por catálogos de produtos, adicionem itens ao carrinho, realizem compras com pagamento integrado via <b>Stripe</b> e acompanhem o status de seus pedidos em tempo real. Administradores têm acesso a um painel de gerenciamento de produtos, categorias, estoque e pedidos. Este projeto foi elaborado pelo aluno <b>Pedro Henrique de Vasconcellos Franco</b> como parte da disciplina <b>Projeto de Software</b>.
      </div>
    </td>
    <td>
      <div>
        <img src="https://img.shields.io/badge/ShopEase-E--commerce-007ec6?style=for-the-badge&logo=shopify&logoColor=white" alt="ShopEase Logo" width="180px"/>
      </div>
    </td>
  </tr>
</table>

---

## 🚧 Status do Projeto

[![Versão](https://img.shields.io/badge/Versão-v1.0.0-blue?style=for-the-badge)](https://github.com/PedroHVFranco/Shopease/releases)
![React](https://img.shields.io/badge/React-18.3.1-007ec6?style=for-the-badge&logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5.4.5-007ec6?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-5.2.0-007ec6?style=for-the-badge&logo=vite&logoColor=white)
![TailwindCSS](https://img.shields.io/badge/Tailwind_CSS-3.4.4-007ec6?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Java](https://img.shields.io/badge/Java-17-007ec6?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-3.3.5-007ec6?style=for-the-badge&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-16-007ec6?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-26.1.4-007ec6?style=for-the-badge&logo=docker&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-Payments-007ec6?style=for-the-badge&logo=stripe&logoColor=white)
![Vercel](https://img.shields.io/badge/Vercel-Deploy-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-Deploy-0B0D0E?style=for-the-badge&logo=railway&logoColor=white)
![GitHub license](https://img.shields.io/github/license/PedroHVFranco/Shopease?style=for-the-badge&color=007ec6&logo=opensourceinitiative)

---

## 📚 Índice

- [Links Úteis](#-links-úteis)
- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades Principais](#-funcionalidades-principais)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Arquitetura](#-arquitetura)
- [Instalação e Execução](#-instalação-e-execução)
  - [Pré-requisitos](#pré-requisitos)
  - [Variáveis de Ambiente](#-variáveis-de-ambiente)
  - [Instalação de Dependências](#-instalação-de-dependências)
  - [Inicialização do Banco de Dados](#-inicialização-do-banco-de-dados-postgresql)
  - [Como Executar a Aplicação](#-como-executar-a-aplicação)
  - [Docker Compose](#-execução-local-completa-com-docker-compose)
- [Deploy](#-deploy)
- [Estrutura de Pastas](#-estrutura-de-pastas)
- [Demonstração](#-demonstração)
- [Testes](#-testes)
- [Documentação de Projeto](#documentação-de-projeto)
- [Documentações Utilizadas](#-documentações-utilizadas)
- [Autores](#-autores)
- [Contribuição](#-contribuição)
- [Agradecimentos](#-agradecimentos)
- [Licença](#-licença)

---

## 🔗 Links Úteis

* 🌐 **Demo Online:** [Acesse a Aplicação Web](https://shopease.vercel.app)
  > 💻 Frontend hospedado na **Vercel** — acesso público à plataforma de e-commerce.
* 📖 **API Docs (Swagger):** [Documentação da API REST](https://shopease-api.railway.app/swagger-ui.html)
  > 📚 Documentação interativa dos endpoints gerada automaticamente pelo **SpringDoc OpenAPI 3**.
* 🗂️ **Especificação do Projeto:** [ShopEase.pdf](./ShopEase.pdf)
  > 📄 Documento de especificação original com visão de domínio, requisitos e regras de negócio.

---

## 📝 Sobre o Projeto

O **ShopEase** nasceu da necessidade de oferecer uma experiência de compra de produtos eletrônicos simples, rápida e segura para o consumidor brasileiro. Em um mercado cada vez mais competitivo, a plataforma foi projetada para se destacar pela **usabilidade**, **performance** e **confiabilidade**.

**Por que ele existe?**
Consumidores enfrentam dificuldades com plataformas de e-commerce lentas, com interfaces confusas e processos de pagamento pouco transparentes. O ShopEase resolve esse problema oferecendo uma jornada de compra fluida, do catálogo ao pós-venda.

**Qual problema ele resolve?**
- Centraliza o catálogo de eletrônicos com busca, filtros por categoria e faixa de preço.
- Simplifica o processo de checkout com pagamento integrado ao Stripe.
- Oferece rastreamento de pedidos em tempo real para o cliente.
- Fornece ao administrador um painel de controle completo para gestão de produtos, estoque e pedidos.

**Contexto:** Projeto acadêmico desenvolvido na disciplina **Projeto de Software** da **PUC Minas**, utilizando práticas modernas de engenharia de software, modelagem UML e arquitetura em camadas.

---

## ✨ Funcionalidades Principais

- 🔐 **Autenticação Segura:** Cadastro, login e controle de acesso via **JWT** com roles (`ROLE_CLIENT`, `ROLE_ADMIN`).
- 🛍️ **Catálogo de Produtos:** Navegação por categorias, busca por nome/marca e filtros por faixa de preço.
- 🛒 **Carrinho de Compras:** Adição, remoção e atualização de quantidades com recálculo automático do subtotal.
- 💳 **Checkout e Pagamento:** Processo de checkout com endereço de entrega e pagamento seguro via **Stripe** (cartão de crédito/débito, Pix, boleto).
- 📦 **Acompanhamento de Pedidos:** Status em tempo real (confirmado → enviado → entregue → cancelado).
- ⚙️ **Painel Administrativo:** Criação, edição, ativação/desativação de produtos e controle de estoque.
- 📊 **Dashboard de Métricas:** Visualização de vendas, receita e pedidos em tempo real.
- 📨 **Notificações por E-mail:** Envio de e-mails transacionais de confirmação via **SendGrid**.

---

## 🛠 Tecnologias Utilizadas

As seguintes ferramentas, frameworks e bibliotecas foram utilizadas na construção do ShopEase.

### 💻 Front-end

| Tecnologia | Versão | Uso |
|---|---|---|
| **React** | 18.3.1 | Biblioteca principal de UI (SPA) |
| **TypeScript** | 5.4.5 | Superset tipado do JavaScript |
| **Tailwind CSS** | 3.4.4 | Framework de estilização utilitária |
| **Zustand** | 4.5.2 | Gerenciamento de estado global (carrinho, auth) |
| **React Router DOM** | 6.23.1 | Roteamento client-side |
| **Axios** | 1.7.2 | Cliente HTTP para chamadas à API REST |
| **Vite** | 5.2.0 | Build tool e servidor de desenvolvimento |
| **Stripe.js** | 3.5.0 | Tokenização segura de dados de pagamento |

### 🖥️ Back-end

| Tecnologia | Versão | Uso |
|---|---|---|
| **Java** | 17 (JDK) | Linguagem principal do backend |
| **Spring Boot** | 3.3.5 | Framework principal da API REST |
| **Spring Security** | 6.3.1 | Autenticação e autorização (JWT) |
| **Spring Data JPA** | 3.3.5 | ORM / repositórios com Hibernate |
| **Flyway** | 10.15.0 | Versionamento e migrações do banco de dados |
| **PostgreSQL** | 16 | Banco de dados relacional principal |
| **SpringDoc OpenAPI** | 2.5.0 | Documentação automática da API (Swagger UI) |
| **Maven** | 3.9.8 | Gerenciador de dependências e build |

### ⚙️ Infraestrutura & DevOps

| Tecnologia | Uso |
|---|---|
| **Docker 26.1.4 + Docker Compose** | Containerização do ambiente de desenvolvimento local |
| **Vercel** | Hospedagem e deploy automático do Front-end (CI/CD via GitHub) |
| **Railway** | Hospedagem do Back-end (Spring Boot JAR) e PostgreSQL em produção |
| **GitHub Actions** | Pipeline de CI/CD para testes e build automatizados |
| **Stripe API** | Processamento de pagamentos (PCI-DSS Compliant) |
| **SendGrid API** | Envio de e-mails transacionais |

---

## 🏗 Arquitetura

O ShopEase adota uma **arquitetura em camadas (Layered Architecture)** no backend, com princípios de separação de responsabilidades inspirados em Clean Architecture. O frontend é uma **SPA (Single Page Application)** que se comunica exclusivamente com a API REST via HTTPS.

### Decisões Arquiteturais

| Decisão | Justificativa |
|---------|---------------|
| Arquitetura em camadas (Controller → Service → Repository) | Separação de responsabilidades clara, alta testabilidade e facilidade de manutenção. |
| JWT stateless para autenticação | Escalabilidade horizontal sem necessidade de sessões server-side. |
| Flyway para migrações de banco | Controle versionado e auditável do schema do banco de dados. |
| React SPA + API REST separada | Desacoplamento total entre frontend e backend, permitindo evolução independente. |
| Stripe para pagamentos | Conformidade PCI-DSS delegada ao provedor, reduzindo responsabilidade de segurança do ShopEase. |

### Exemplos de Diagramas

| Diagrama de Contexto C4 (Level 1) | Diagrama de Componentes |
| :---: | :---: |
| <img width="669" height="659" alt="Arq_C4_Context" src="https://github.com/user-attachments/assets/d1f83089-4cb6-47e6-8460-2ec1bc65c783" /> | <img width="1065" height="801" alt="Diagrama_Componentes" src="https://github.com/user-attachments/assets/fdaffbc0-fe76-428a-8f89-8c219bb910ce" /> |
| **Diagrama de Implantação** | **Diagrama de Classes** |
| <img width="768" height="1029" alt="Diagrama_Implantacao" src="https://github.com/user-attachments/assets/3a0c7e6f-4794-432d-b2bd-b6eb17fe64e7" /> | <img width="1133" height="1410" alt="Diagrama_Classes" src="https://github.com/user-attachments/assets/e423d416-ff85-4829-a676-c830d8ee4b98" /> |
| **DER (Modelo Lógico)** | **Diagrama de Estados — Pedido** |
| <img width="1576" height="1163" alt="DER_ShopEase" src="https://github.com/user-attachments/assets/e3ebc6b2-d2e0-4b19-9837-d2dd88a5a5f8" /> | <img width="673" height="1117" alt="Estados_Pedido" src="https://github.com/user-attachments/assets/225dbf08-6533-4d65-89b2-7c8358366df1" /> |

---

## 🔧 Instalação e Execução

### Pré-requisitos

* **Java JDK 17** ou superior — necessário para o **Back-end Spring Boot**
* **Node.js** LTS (v18.x ou superior) — necessário para o **Front-end React**
* **npm** ou **yarn** — gerenciador de pacotes Node.js
* **Docker** (recomendado) — para rodar o PostgreSQL localmente via container

---

### 🔑 Variáveis de Ambiente

#### Back-end (Spring Boot)

Configure em `backend/src/main/resources/application.yml` ou como variáveis de ambiente:

| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `SERVER_PORT` | Porta onde o Back-end será executado | `8080` |
| `SPRING_DATASOURCE_URL` | URL de conexão JDBC (PostgreSQL) | `jdbc:postgresql://localhost:5432/shopease` |
| `SPRING_DATASOURCE_USERNAME` | Usuário do banco de dados | `postgres` |
| `SPRING_DATASOURCE_PASSWORD` | Senha do banco de dados | `shopease_secret_123` |
| `JWT_SECRET` | Chave secreta para assinatura dos tokens JWT | `shopease_jwt_key_256bits_base64` |
| `JWT_EXPIRATION_MS` | Tempo de expiração do JWT em milissegundos | `86400000` (24h) |
| `STRIPE_SECRET_KEY` | Chave secreta da API Stripe | `sk_live_...` |
| `STRIPE_WEBHOOK_SECRET` | Chave de verificação dos webhooks Stripe | `whsec_...` |
| `SENDGRID_API_KEY` | Chave da API SendGrid para envio de e-mails | `SG....` |
| `SENDGRID_FROM_EMAIL` | E-mail remetente das notificações | `noreply@shopease.com.br` |

#### Front-end (React + Vite)

Crie um arquivo **`.env`** na raiz da pasta `/frontend`:

| Variável | Descrição | Exemplo |
| :--- | :--- | :--- |
| `VITE_API_URL` | URL base do Back-end Spring Boot | `http://localhost:8080/api` |
| `VITE_STRIPE_PUBLISHABLE_KEY` | Chave pública do Stripe para Stripe.js | `pk_live_...` |

---

### 📦 Instalação de Dependências

1. **Clone o Repositório:**

```bash
git clone https://github.com/PedroHVFranco/Shopease.git
cd Shopease
```

2. **Front-end (React):**

```bash
cd frontend
npm install
cd ..
```

3. **Back-end (Spring Boot + Maven):**

```bash
cd backend
./mvnw clean install
cd ..
```

---

### 💾 Inicialização do Banco de Dados (PostgreSQL)

Rode o container PostgreSQL via Docker:

```bash
docker run --name shopease_db \
  -e POSTGRES_USER=postgres \
  -e POSTGRES_PASSWORD=shopease_secret_123 \
  -e POSTGRES_DB=shopease \
  -p 5432:5432 \
  -d postgres:16
```

> As migrações de schema são aplicadas automaticamente pelo **Flyway** na inicialização do Back-end.

---

### ⚡ Como Executar a Aplicação

Execute em dois terminais separados:

#### Terminal 1: Back-end (Spring Boot)

```bash
cd backend
./mvnw spring-boot:run
```
🚀 *API disponível em **http://localhost:8080** | Swagger UI em **http://localhost:8080/swagger-ui.html***

#### Terminal 2: Front-end (React + Vite)

```bash
cd frontend
npm run dev
```
🎨 *Front-end disponível em **http://localhost:5173***

---

### 🐳 Execução Local Completa com Docker Compose

Para subir todos os serviços (front-end, back-end e banco) de uma vez:

```bash
docker-compose up --build -d
```

Verifique os containers:

```bash
docker ps
```

Acesse em: **http://localhost:3000**

Para encerrar:

```bash
docker-compose down
```

---

## 🚀 Deploy

O ShopEase utiliza deploy automatizado via **GitHub Actions** integrado à **Vercel** (frontend) e **Railway** (backend + banco).

1. **Build do Front-end (Vercel):**

```bash
cd frontend
npm run build
# Artefatos gerados em /dist — enviados automaticamente para a Vercel via GitHub push
```

2. **Build do Back-end (Railway):**

```bash
cd backend
./mvnw clean package
# Gera shopease-api-1.0.0.jar em /target — implantado no Railway via Dockerfile
```

3. **Variáveis de Ambiente em Produção:**

| Plataforma | Onde configurar |
|---|---|
| Vercel (frontend) | Project Settings → Environment Variables |
| Railway (backend) | Project → Variables |

> 🔑 Certifique-se de configurar `VITE_API_URL` apontando para a URL de produção do Railway, e as variáveis `STRIPE_*`, `SENDGRID_*` e `JWT_*` no Railway.

---

## 📂 Estrutura de Pastas

```
shopease/
├── .github/
│   └── workflows/
│       ├── ci-frontend.yml      # Pipeline CI: lint + testes do React
│       └── ci-backend.yml       # Pipeline CI: build + testes do Spring Boot
├── docker-compose.yml           # Orquestração local: front + back + db
├── README.md                    # Documentação principal
├── ShopEase.pdf                 # Especificação original do projeto
│
├── frontend/                    # Aplicação React (SPA)
│   ├── .env.example
│   ├── Dockerfile
│   ├── vite.config.ts
│   ├── tailwind.config.js
│   ├── tsconfig.json
│   └── src/
│       ├── components/          # Componentes reutilizáveis (ProductCard, CartDrawer, etc.)
│       ├── pages/               # Páginas (Home, ProductDetail, Checkout, Orders, Admin)
│       ├── store/               # Estado global com Zustand (cartStore, authStore)
│       ├── services/            # Chamadas HTTP com Axios (productService, orderService)
│       ├── hooks/               # Hooks personalizados (useAuth, useCart)
│       ├── types/               # Tipos TypeScript (Product, Order, User, etc.)
│       └── utils/               # Funções utilitárias (formatCurrency, formatDate)
│
└── backend/                     # API REST Spring Boot
    ├── .env.example
    ├── Dockerfile
    ├── pom.xml
    └── src/
        ├── main/java/com/shopease/
        │   ├── controller/      # Endpoints REST (ProductController, OrderController, etc.)
        │   ├── service/         # Regras de negócio (ProductService, OrderService, PaymentService)
        │   ├── repository/      # Repositórios JPA (ProductRepository, OrderRepository, etc.)
        │   ├── model/           # Entidades JPA (Product, Order, User, Cart, Payment, etc.)
        │   ├── dto/             # Data Transfer Objects (ProductDTO, OrderDTO, CartDTO, etc.)
        │   ├── config/          # Configurações (SecurityConfig, CorsConfig, SwaggerConfig)
        │   ├── security/        # JWT Filter, UserDetailsService, autenticação
        │   └── exception/       # GlobalExceptionHandler, ResourceNotFoundException
        └── main/resources/
            ├── application.yml
            ├── application-dev.yml
            ├── application-prod.yml
            └── db/migration/    # Scripts Flyway (V1__create_schema.sql, V2__seed_data.sql, etc.)
```

---

## 🎥 Demonstração

### 🌐 Aplicação Web

| Tela | Captura de Tela |
| :---: | :---: |
| **Página Inicial — Catálogo de Produtos** | **Página de Detalhes do Produto** |
| <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Catálogo ShopEase" width="120px" height="120px"> | <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Detalhe do Produto" width="120px" height="120px"> |
| **Carrinho de Compras** | **Checkout e Pagamento (Stripe)** |
| <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Carrinho ShopEase" width="120px" height="120px"> | <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Checkout ShopEase" width="120px" height="120px"> |
| **Acompanhamento de Pedidos** | **Painel Administrativo** |
| <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Pedidos ShopEase" width="120px" height="120px"> | <img src="https://joaopauloaramuni.github.io/image/aramunilogo.png" alt="Admin ShopEase" width="120px" height="120px"> |

### 💻 Exemplo de Saída da API (cURL)

```bash
# Busca produtos da categoria "Smartphones" com autenticação JWT
curl -X GET 'https://shopease-api.railway.app/api/products?category=smartphones&minPrice=500&maxPrice=3000' \
     -H 'Authorization: ******'
```

**Saída Esperada:**
```json
{
  "content": [
    {
      "id": 42,
      "name": "Samsung Galaxy S24 Ultra",
      "brand": "Samsung",
      "price": 2499.99,
      "stockQty": 15,
      "category": "Smartphones",
      "active": true
    },
    {
      "id": 43,
      "name": "Apple iPhone 15 Pro",
      "brand": "Apple",
      "price": 2899.99,
      "stockQty": 8,
      "category": "Smartphones",
      "active": true
    }
  ],
  "totalElements": 12,
  "totalPages": 2,
  "page": 0,
  "size": 10
}
```

---

## 🧪 Testes

### Testes Unitários e de Integração (Back-end)

```bash
cd backend
./mvnw test
```
*Ferramentas: **JUnit 5**, **Mockito**, **Spring Boot Test**, **TestContainers** (PostgreSQL)*

### Testes Unitários (Front-end)

```bash
cd frontend
npm run test
```
*Ferramentas: **Vitest**, **React Testing Library***

### Testes End-to-End (E2E)

```bash
cd frontend
npm run test:e2e
```
*Ferramenta: **Playwright** — cenários cobrindo fluxo de compra completo (login → catálogo → carrinho → checkout → pedido confirmado)*

---

## 🔗 Documentações Utilizadas

* 📖 **Front-end:** [Documentação Oficial do React 18](https://react.dev/reference/react)
* 📖 **TypeScript:** [Manual do TypeScript](https://www.typescriptlang.org/docs/)
* 📖 **Tailwind CSS:** [Documentação Oficial](https://tailwindcss.com/docs)
* 📖 **Zustand:** [Guia de Uso do Zustand](https://docs.pmnd.rs/zustand/getting-started/introduction)
* 📖 **Back-end:** [Documentação Oficial do Spring Boot 3.3](https://docs.spring.io/spring-boot/docs/3.3.5/reference/html/)
* 📖 **Spring Security:** [Spring Security Reference](https://docs.spring.io/spring-security/reference/)
* 📖 **Flyway:** [Documentação do Flyway](https://flymigrate.red/documentation/)
* 📖 **Stripe:** [Stripe API Reference](https://stripe.com/docs/api)
* 📖 **SendGrid:** [SendGrid Email API Docs](https://docs.sendgrid.com/)
* 📖 **Docker:** [Documentação de Referência do Docker](https://docs.docker.com/)
* 📖 **Conventional Commits:** [Padrão de Mensagens de Commit](https://www.conventionalcommits.org/en/v1.0.0/)
* 📖 **PlantUML:** [Referência PlantUML](https://plantuml.com)

---

## 👥 Autores

| 👤 Nome | 🖼️ Foto | :octocat: GitHub | 💼 LinkedIn | 📤 Gmail |
|---------|----------|-----------------|-------------|-----------|
| Pedro Henrique de Vasconcellos Franco | <div align="center"><img src="https://github.com/PedroHVFranco.png" width="70px" height="70px" style="border-radius:50%"></div> | <div align="center"><a href="https://github.com/PedroHVFranco"><img src="https://joaopauloaramuni.github.io/image/github6.png" width="50px" height="50px"></a></div> | <div align="center"><a href="https://www.linkedin.com/in/pedrovasconcellosfranco"><img src="https://joaopauloaramuni.github.io/image/linkedin2.png" width="50px" height="50px"></a></div> | <div align="center"><a href="mailto:pedro.franco@sga.pucminas.br"><img src="https://joaopauloaramuni.github.io/image/gmail3.png" width="50px" height="50px"></a></div> |

---

## 🤝 Contribuição

1. Faça um `fork` do projeto.
2. Crie uma branch para sua feature (`git checkout -b feature/minha-feature`).
3. Commit suas mudanças (`git commit -m 'feat: Adiciona nova funcionalidade X'`). **(Utilize [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/))**
4. Faça o `push` para a branch (`git push origin feature/minha-feature`).
5. Abra um **Pull Request (PR)**.

---

## 🙏 Agradecimentos

* [**Engenharia de Software PUC Minas**](https://www.instagram.com/engsoftwarepucminas/) — Pelo apoio institucional e fomento à inovação.
* [**Prof. Dr. João Paulo Aramuni**](https://github.com/joaopauloaramuni) — Pelos valiosos ensinamentos sobre **Arquitetura de Software**, **Padrões de Projeto** e modelagem UML.
* [**Stripe Docs**](https://stripe.com/docs) — Pela documentação clara e exemplos práticos de integração de pagamentos.
* [**Spring Community**](https://spring.io/community) — Pela extensa base de conhecimento e suporte da comunidade.

---

## 📄 Licença

Este projeto é distribuído sob a **[Licença MIT](./LICENSE)**.

---

---

# Documentação de Projeto

**para o sistema**

**ShopEase — Plataforma de E-commerce**

**Versão 1.0**

Projeto de sistema elaborado pelo aluno **Pedro Henrique de Vasconcellos Franco**

como parte da disciplina **Projeto de Software**.


## Tabela de Conteúdo

1. [Introdução](#1-introdução)
2. [Modelos de Usuário e Requisitos](#2-modelos-de-usuário-e-requisitos)
   - [2.1 Descrição de Atores](#21-descrição-de-atores)
   - [2.2 Modelo de Casos de Uso](#22-modelo-de-casos-de-uso)
   - [2.3 Diagrama de Sequência do Sistema e Contrato de Operações](#23-diagrama-de-sequência-do-sistema-e-contrato-de-operações)
3. [Modelos de Projeto](#3-modelos-de-projeto)
   - [3.1 Arquitetura](#31-arquitetura)
   - [3.2 Diagrama de Componentes e Implantação](#32-diagrama-de-componentes-e-implantação)
   - [3.3 Diagrama de Classes](#33-diagrama-de-classes)
   - [3.4 Diagramas de Sequência](#34-diagramas-de-sequência)
   - [3.5 Diagramas de Comunicação](#35-diagramas-de-comunicação)
   - [3.6 Diagramas de Estados](#36-diagramas-de-estados)
4. [Modelos de Dados](#4-modelos-de-dados)

---

# 1. Introdução

Este documento agrega: (1) a elaboração e revisão de modelos de domínio e (2) modelos de projeto para o sistema **ShopEase — Plataforma de E-commerce**. A referência principal para a descrição geral do problema, domínio e requisitos do sistema é o documento de especificação que descreve a visão de domínio do sistema.

O **ShopEase** é uma plataforma B2C de e-commerce voltada para a venda de produtos eletrônicos. O sistema permite que clientes naveguem por catálogos de produtos, adicionem itens ao carrinho, realizem compras com pagamento integrado via Stripe e acompanhem o status de seus pedidos em tempo real. Administradores têm acesso a um painel de gerenciamento de produtos, categorias, estoque e pedidos.

O sistema é composto por:

- **Frontend:** Aplicação React 18 + TypeScript + Tailwind CSS, hospedada na Vercel.
- **Backend:** API REST Spring Boot 3.3 + Java 17 + Spring Security, hospedada no Railway.
- **Banco de Dados:** PostgreSQL 16, gerenciado no Railway.
- **Integrações externas:** Stripe (processamento de pagamentos), SendGrid (e-mails transacionais).

Todos os diagramas deste documento foram elaborados utilizando **PlantUML** (https://plantuml.com), conforme exigência da disciplina.

---

# 2. Modelos de Usuário e Requisitos

## 2.1 Descrição de Atores

### Ator 1: Cliente

O **Cliente** é o usuário primário do sistema ShopEase. Representa qualquer pessoa física que acessa a plataforma com o objetivo de comprar produtos eletrônicos.

**Responsabilidades:**
- Cadastrar-se e autenticar-se na plataforma.
- Navegar e buscar produtos no catálogo por categoria, nome ou faixa de preço.
- Adicionar produtos ao carrinho de compras e gerenciar quantidades.
- Realizar checkout, informar endereço de entrega e efetuar pagamento.
- Acompanhar o status de seus pedidos em tempo real.
- Cancelar pedidos dentro do período permitido.

**Pré-condições de acesso:** Possuir acesso à internet e um endereço de e-mail válido.

---

### Ator 2: Administrador

O **Administrador** é o usuário responsável pela gestão operacional da plataforma. Representa o varejista ou a equipe de operações do ShopEase.

**Responsabilidades:**
- Cadastrar, editar, ativar e desativar produtos no catálogo.
- Gerenciar categorias de produtos.
- Controlar e atualizar o estoque de produtos.
- Visualizar todos os pedidos realizados na plataforma.
- Atualizar o status do ciclo de vida dos pedidos (confirmado, enviado, entregue, cancelado).
- Acessar o dashboard com métricas de vendas e relatórios.

**Pré-condições de acesso:** Possuir credenciais com perfil `ROLE_ADMIN` configurado no sistema.

---

### Ator 3: Sistema de Pagamento — Stripe (Ator Externo)

O **Sistema de Pagamento** é um ator externo representado pelo gateway **Stripe**. Ele é responsável pelo processamento seguro de todas as transações financeiras da plataforma.

**Responsabilidades:**
- Receber e processar dados de pagamento (cartão de crédito/débito, Pix, boleto bancário).
- Retornar confirmação (`succeeded`) ou rejeição (`failed`) do pagamento ao ShopEase via API REST.
- Emitir webhooks de eventos de pagamento (pagamento confirmado, expirado, reembolsado).
- Armazenar dados de pagamento de forma segura (PCI-DSS Compliance).

**Pré-condições:** API Key válida do Stripe configurada como variável de ambiente no backend.

---

## 2.2 Modelo de Casos de Uso

### Diagrama de Casos de Uso

O sistema ShopEase possui 6 casos de uso principais, distribuídos entre os três atores identificados.

<img width="1003" height="1215" alt="UC_ShopEase" src="https://github.com/user-attachments/assets/3e3ce8d7-9199-4a74-9ba9-f324b2f02a06" />

### Descrição dos Casos de Uso

| ID | Nome | Ator Principal | Descrição Resumida |
|----|------|----------------|--------------------|
| UC-01 | Cadastrar/Autenticar Usuário | Cliente, Admin | Permite que novos usuários se cadastrem e que usuários existentes realizem login com JWT. |
| UC-02 | Navegar e Buscar Produtos | Cliente, Admin | Permite navegar pelo catálogo por categoria e realizar buscas por nome, marca ou faixa de preço. |
| UC-03 | Gerenciar Carrinho de Compras | Cliente | Permite adicionar, remover e atualizar quantidades de produtos no carrinho de compras. |
| UC-04 | Realizar Checkout e Pagamento | Cliente | Permite ao cliente confirmar o pedido, informar endereço de entrega e efetuar pagamento via Stripe. |
| UC-05 | Acompanhar Pedido | Cliente, Admin | Permite ao cliente visualizar o status do pedido e ao admin atualizar o ciclo de vida do pedido. |
| UC-06 | Gerenciar Catálogo (Admin) | Administrador | Permite ao admin criar, editar, ativar/desativar produtos, gerenciar categorias e controlar estoque. |

---

## 2.3 Diagrama de Sequência do Sistema e Contrato de Operações

Nesta seção são apresentados os Diagramas de Sequência do Sistema (DSS) para 3 Casos de Uso, com os respectivos Contratos de Operação.

---

### DSS-01: Autenticar Usuário (UC-01)

<img width="580" height="465" alt="DSS01_AutenticarUsuario" src="https://github.com/user-attachments/assets/05ef0ef5-9367-4d41-952e-4653fd5054ff" />

**Contrato de Operação — `autenticarUsuario`**

| **Contrato** | CO-01 |
|---|---|
| **Operação** | `autenticarUsuario(email: String, senha: String): String` |
| **Referências cruzadas** | UC-01 — Cadastrar/Autenticar Usuário |
| **Pré-condições** | 1. O usuário deve estar previamente cadastrado no sistema. 2. O campo `email` deve ter formato de e-mail válido (RFC 5322). 3. O usuário deve estar com status `active = true`. |
| **Pós-condições** | 1. Um token JWT válido é gerado e retornado ao cliente. 2. O token contém os claims: `userId`, `email` e `role`. 3. O token tem validade de 24 horas (configurável via `JWT_EXPIRATION_MS`). |

---

### DSS-02: Adicionar Produto ao Carrinho (UC-03)

<img width="648" height="506" alt="DSS02_AdicionarCarrinho" src="https://github.com/user-attachments/assets/a07f02c4-68c1-467d-af7d-a1c3d41a4c45" />

**Contrato de Operação — `adicionarAoCarrinho`**

| **Contrato** | CO-02 |
|---|---|
| **Operação** | `adicionarAoCarrinho(produtoId: Long, quantidade: Integer): CartDTO` |
| **Referências cruzadas** | UC-03 — Gerenciar Carrinho de Compras |
| **Pré-condições** | 1. O cliente deve estar autenticado (token JWT válido). 2. O produto com `produtoId` deve existir e ter `active = true`. 3. A `quantidade` deve ser maior que zero. 4. O estoque disponível (`stock_qty`) deve ser maior ou igual à `quantidade` solicitada. |
| **Pós-condições** | 1. O item é adicionado ao carrinho (ou a quantidade é incrementada, caso já exista). 2. O subtotal do item (`unitPrice × quantity`) e o total do carrinho são recalculados. 3. O estoque não é decrementado neste momento (apenas na confirmação do pedido, UC-04). 4. O campo `updatedAt` do carrinho é atualizado com a data/hora atual. |

---

### DSS-03: Realizar Checkout e Pagamento (UC-04)

<img width="1020" height="603" alt="DSS03_RealizarCheckout" src="https://github.com/user-attachments/assets/70347b69-d288-427e-b8ed-ead23fb84b7f" />

**Contrato de Operação — `confirmarPagamento`**

| **Contrato** | CO-03 |
|---|---|
| **Operação** | `confirmarPagamento(checkoutId: Long, dadosPagamento: PaymentDTO): OrderDTO` |
| **Referências cruzadas** | UC-04 — Realizar Checkout e Pagamento |
| **Pré-condições** | 1. O cliente deve estar autenticado (token JWT válido). 2. O carrinho deve conter pelo menos 1 item com estoque disponível. 3. Um endereço de entrega válido deve ter sido informado e validado. 4. Os dados de pagamento devem ser válidos (cartão não expirado, dados completos) e tokenizados pelo Stripe.js. |
| **Pós-condições** | 1. Um novo `Order` é criado com status `CONFIRMED`. 2. Os itens do carrinho são convertidos em `OrderItem`s, preservando o `unitPrice` no momento da compra. 3. O `stock_qty` dos produtos é decrementado com as quantidades do pedido. 4. Um `Payment` com `status = APPROVED` e o `stripePaymentIntentId` é criado e associado ao pedido. 5. O carrinho do cliente é esvaziado (`cart_items` deletados). 6. Um e-mail de confirmação com detalhes do pedido é enviado ao cliente via SendGrid. |

---

# 3. Modelos de Projeto

## 3.1 Arquitetura

O ShopEase adota uma **arquitetura em camadas (Layered Architecture)** no backend, com princípios de separação de responsabilidades inspirados em Clean Architecture. O frontend é uma **SPA (Single Page Application)** que se comunica exclusivamente com a API REST via HTTPS.

### Decisões Arquiteturais

| Decisão | Justificativa |
|---------|---------------|
| Arquitetura em camadas (Controller → Service → Repository) | Separação de responsabilidades clara, alta testabilidade e facilidade de manutenção. |
| JWT stateless para autenticação | Escalabilidade horizontal sem necessidade de sessões server-side. |
| Flyway para migrações de banco | Controle versionado e auditável do schema do banco de dados. |
| React SPA + API REST separada | Desacoplamento total entre frontend e backend, permitindo evolução independente e possível expansão para mobile. |
| Stripe para pagamentos | Conformidade PCI-DSS delegada ao provedor, reduzindo responsabilidade de segurança do ShopEase. |

### Diagrama de Contexto C4 (Level 1)

<img width="669" height="659" alt="Arq_C4_Context" src="https://github.com/user-attachments/assets/d1f83089-4cb6-47e6-8460-2ec1bc65c783" />

## 3.2 Diagrama de Componentes e Implantação

### Diagrama de Componentes

<img width="1065" height="801" alt="Diagrama_Componentes" src="https://github.com/user-attachments/assets/fdaffbc0-fe76-428a-8f89-8c219bb910ce" />

### Diagrama de Implantação

<img width="768" height="1029" alt="Diagrama_Implantacao" src="https://github.com/user-attachments/assets/3a0c7e6f-4794-432d-b2bd-b6eb17fe64e7" />

## 3.3 Diagrama de Classes

<img width="1133" height="1410" alt="Diagrama_Classes" src="https://github.com/user-attachments/assets/e423d416-ff85-4829-a676-c830d8ee4b98" />

## 3.4 Diagramas de Sequência

### SD-01: Realizar Checkout e Pagamento (UC-04) — Detalhado

<img width="1433" height="1230" alt="SD01_Checkout_Detalhado" src="https://github.com/user-attachments/assets/f53c28b7-0e76-435b-a1fb-24963bc49fed" />

## 3.5 Diagramas de Comunicação

### Diagrama de Comunicação — Realizar Checkout (UC-04)

<img width="2148" height="650" alt="Comunicacao_Checkout" src="https://github.com/user-attachments/assets/9c3f90dc-3588-4def-96d1-7355410ab97c" />

## 3.6 Diagramas de Estados

### Diagrama de Estados — Ciclo de Vida do Pedido

<img width="673" height="1117" alt="Estados_Pedido" src="https://github.com/user-attachments/assets/225dbf08-6533-4d65-89b2-7c8358366df1" />

# 4. Modelos de Dados

O ShopEase utiliza **PostgreSQL 16** como SGBD relacional. As migrações são versionadas e gerenciadas pelo **Flyway**, garantindo consistência e rastreabilidade do schema entre ambientes (dev, staging, produção).

### Diagrama Entidade-Relacionamento (Modelo Lógico)

<img width="1576" height="1163" alt="DER_ShopEase" src="https://github.com/user-attachments/assets/e3ebc6b2-d2e0-4b19-9837-d2dd88a5a5f8" />
