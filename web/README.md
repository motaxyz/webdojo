# 🧪 Testes Automatizados -- WebDojo (Cypress)

Este repositório contém a suíte de **testes automatizados end-to-end**
da aplicação **WebDojo**, utilizando o framework **Cypress**.\
A aplicação WebDojo e os testes estão no **mesmo repositório**,
permitindo uma fácil integração entre o ambiente de desenvolvimento e a
execução dos testes.

------------------------------------------------------------------------

## 📦 Pré-requisitos

Certifique-se de ter instalado:

-   **Node.js** (versão 16+ recomendada)
-   **npm**
-   **Google Chrome**, **Edge** ou **Electron**

------------------------------------------------------------------------

## 🚀 Executando a Aplicação WebDojo

Antes de rodar os testes, é necessário subir a aplicação WebDojo.\
No diretório raiz, execute:

``` bash
npm run dev
```

A aplicação será iniciada utilizando `serve -s dist -p 3000` e ficará
disponível em:

    http://localhost:3000

------------------------------------------------------------------------

## 🧪 Executando os Testes com Cypress

A suíte de testes pode ser executada em modo headless ou interativo.

### ▶️ Executar todos os testes (modo headless)

``` bash
npm test
```

Configurações usadas:

-   `viewportWidth: 1940`
-   `viewportHeight: 900`

------------------------------------------------------------------------

### 🖥️ Abrir o Cypress em modo interativo (UI)

``` bash
npm run test:ui
```

Ideal para desenvolvimento, debug e visualização em tempo real.

------------------------------------------------------------------------

### 🔐 Rodar somente os testes de Login (desktop)

``` bash
npm run test:login
```

Executa apenas:

    cypress/e2e/login.cy.js

Viewport: `1940x900`.

------------------------------------------------------------------------

### 📱 Rodar somente os testes de Login (mobile)

``` bash
npm run test:login:mobile
```

Viewport: `414x896`.

------------------------------------------------------------------------

## 📁 Estrutura do Projeto Cypress

    cypress/
    │
    ├── e2e/
    │     └── (arquivos de testes .cy.js)
    │
    ├── fixtures/
    │     ├── cep.json
    │     ├── consultancy.json
    │     └── documentlorempdf.pdf
    │
    ├── support/
    │     ├── actions/
    │     │     └── consultancy.actions.js
    │     ├── commands.js
    │     ├── e2e.js
    │     └── utils.js

------------------------------------------------------------------------

## 📌 Descrição das Pastas

### **📂 e2e/**

Local onde ficam os arquivos de testes Cypress (`*.cy.js`),
representando cenários e fluxos completos da aplicação WebDojo.

### **📂 fixtures/**

Armazena dados estáticos utilizados nos testes, como:

-   Arquivos `.json`
-   Dados mockados
-   PDFs e arquivos para upload

### **📂 support/**

Contém funções auxiliares e configurações globais.

-   **actions/**: ações encapsuladas\
-   **commands.js**: comandos customizados\
-   **e2e.js**: scripts executados antes ou durante os testes\
-   **utils.js**: utilitários usados por múltiplos testes

------------------------------------------------------------------------

## 🧱 Arquitetura e Boas Práticas

-   ✔ Page Actions para organizar ações repetitivas\
-   ✔ Fixtures para dados controlados\
-   ✔ Modularização em `utils.js` e `commands.js`\
-   ✔ Estrutura limpa e escalável

------------------------------------------------------------------------

## 🛠️ Tecnologias Utilizadas

-   Cypress\
-   Node.js\
-   JavaScript\
-   Serve

------------------------------------------------------------------------

## 🤝 Como Contribuir

1.  Clone o repositório\
2.  Instale dependências:

``` bash
npm install
```

3.  Inicie a aplicação:

``` bash
npm run dev
```

4.  Execute os testes:

``` bash
npm test
```

Pull requests, issues e sugestões são sempre bem-vindos!
