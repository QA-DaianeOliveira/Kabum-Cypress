# Desafio Técnico - Automação de Testes com Cypress (BDD)

Este projeto contém a automação dos desafios propostos utilizando o framework Cypress com abordagem BDD. A seguir, você encontrará:

- Descrição dos cenários em formato Gherkin (Dado / Quando / Então)
- Instruções de execução dos testes
- Resultados esperados

---

## Tecnologias Utilizadas

- Cypress (https://www.cypress.io/)
- JavaScript
- Node.js
- VS Code

---

## 🚀 Instalação e Execução

### Pré-requisitos:
- Node.js instalado
- Visual Studio Code

### Passos para executar:

1. Clone este repositório ou baixe o projeto.
2. No terminal, dentro da pasta do projeto, execute:

npm install

3. Para abrir o Cypress:

npx cypress open

4. No Cypress, vá até:

cypress/e2e/kabum/spec.cy.js

E clique no teste para rodá-lo

## Estrutura do Projeto

KABUM-CYPRESS/

├── cypress/
│   ├── e2e/
│   │   └── kabum/
│   │       └── spec.cy.js          
│   ├── fixtures/                   
│   └── support/
│       ├── commands.js             
│       └── e2e.js                  
├── node_modules/                   
├── cypress.config.js               
├── package.json                    
└── package-lock.json            
├── README.md  

---

## Desafio 2 - Amazon

### Cenário 1 - Adicionar livro ao carrinho

```gherkin
Funcionalidade: Adição de produto ao carrinho no site Kabum

  Cenário: Usuário busca notebook e adiciona ao carrinho com garantia

    Dado que o usuário acessa o site da Kabum
    E busca pelo termo "notebook"
    Quando ele seleciona o primeiro produto da lista
    E digita um CEP válido para calcular o frete
    E fecha a tela de opções de frete
    E clica no botão "Comprar"
    E escolhe a garantia estendida de 12 meses
    E clica em "Ir para o carrinho"
    Então o produto deve estar corretamente adicionado no carrinho

Resultado esperado

- Modal de frete ebibe opções corretamente
- Produto é incluido no carrinho
- Garantia de 12 meses é aplicada
-Carrinho exibe o produto selecionado

