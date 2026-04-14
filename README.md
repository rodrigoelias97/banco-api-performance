# 🚀 Banco API Performance Tests

## 📌 Introdução

Este repositório contém testes de performance desenvolvidos em
**JavaScript** utilizando o **K6**, com o objetivo de avaliar o
comportamento e a estabilidade da API do projeto
https://github.com/rodrigoelias97/banco-api sob diferentes condições de
carga.

Os testes simulam cenários reais de uso, permitindo identificar
gargalos, validar tempos de resposta e garantir a escalabilidade da
aplicação.

------------------------------------------------------------------------

## 🛠️ Tecnologias Utilizadas

-   **JavaScript**
-   **K6** -- ferramenta para testes de carga e performance
-   **Node.js** (para gerenciamento do ambiente, se necessário)

------------------------------------------------------------------------

## 📂 Estrutura do Repositório

    banco-api-performance/
    │
    ├── config/                      # Arquivo de configuração de variáveis de ambiente
    ├── fixtures/                    # Dados de entrada para os testes (Ex: usuários, payloads)
    ├── helpers/                     # Funções utilitárias reutilizáveis
    ├── tests/                       # Casos de teste organizados por módulo da API
    ├── utils/                       # Funções utilitárias reutilizáveis para interação com a API
    └── README.md                    # Documentação do projeto

------------------------------------------------------------------------

## 🎯 Objetivo de Cada Grupo de Arquivos

-   **config/**\
    Arquivo de configuração de variáveis de ambiente

-   **fixtures/**\
    Dados de entrada para os testes (Ex: usuários, payloads)

-   **helpers/**\
    Funções utilitárias reutilizáveis

-   **tests/**\
    Casos de teste organizados por módulo da API

-   **utils/**\
    Funções utilitárias reutilizáveis para interação com a API

-   **utils/**\
    Funções reutilizáveis.

------------------------------------------------------------------------

## ⚙️ Instalação

### 1. Clonar o repositório

``` bash
git clone https://github.com/rodrigoelias97/banco-api-performance.git
cd banco-api-performance
```

### 2. Instalar o K6

``` bash
npm install
```

------------------------------------------------------------------------

## ▶️ Execução dos Testes

### 🔹 Definir variável de ambiente

Altere o arquivo config.local.json e defina a URL base da API a ser testada:

{
  "baseUrl": "http://localhost:3000"
}

💡 Essas variáveis serão usada dinamicamente nos testes para montar as requisições.

------------------------------------------------------------------------

### 🔹 Executar um teste simples

``` bash
k6 run tests/login.test.js
```

Certifique-se de passar a variável de ambiente BASE_URL, caso não esteja usando um config.local.json ou uma abordagem de carregamento automático.

------------------------------------------------------------------------

### 📊 Execução com Dashboard + Exportação

``` bash
K6_WEB_DASHBOARD=true K6_WEB_DASHBOARD_EXPORT=html-report.html k6 run tests/login.test.js
```

------------------------------------------------------------------------

## 📌 Observações

-   Certifique-se de que a API esteja em execução antes dos testes.
