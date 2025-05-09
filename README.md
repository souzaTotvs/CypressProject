# Instalação Cypress

> Antes de instalar o Cypress, precisa ter o Node.js e o npm (Node Package Manager) instalados.

1. Verifique se o Node.js está instalado:

```
Node -v

Npm -v
```

**Abra o terminal ou prompt (CMD) de comando e digite:**

Se já tiver instalado no seu computador irá retorna a versão que está, ex.

```
C:\Users\rayssa.souza\Documents>node -v
v22.15.0

C:\Users\rayssa.souza\Documents>npm -v
10.9.2
```

2. Se não estiver instalado:
Baixe e instale o Node.js pelo site oficial: 
https://nodejs.org
________________________________________
 # Passo a passo instalção

**Passo 1: Crie uma pasta para seu projeto (caso ainda não** tenha)
>mkdir meu-projeto-cypress
>
>cd meu-projeto-cypress
________________________________________
**Passo 2: Inicialize o projeto Node**
>npm init -y

Isso criará um arquivo package.json.
________________________________________
**Passo 3: Instale o Cypress**
>npm install cypress --save-dev

Esse comando vai baixar o Cypress e adicionar como dependência de desenvolvimento no seu projeto.
________________________________________
# Como abrir o Cypress pela primeira vez
Depois de instalado, abra o Cypress com o comando:

>npx cypress open

Esse comando vai:
•	Abrir a interface gráfica do Cypress (Test Runner)
•	Criar a estrutura de pastas padrão (cypress/, cypress/e2e, etc.) o cypress é uma ferramenta do testes end to end E2E.
________________________________________
Estrutura básica criada
Após abrir o Cypress pela primeira vez, você verá algo assim:
```
meu-projeto-cypress/
├── cypress/
│   ├── e2e/
│   └── support/
├── node_modules/
├── cypress.config.js
└── package.json 
```

Você já pode começar a escrever seus testes na pasta cypress/e2e.
________________________________________
# Testando com um exemplo
Crie um arquivo de teste:
```
touch cypress/e2e/exemplo.cy.js
Adicione o seguinte conteúdo:
js
CopiarEditar
describe('Meu primeiro teste', () => {
  it('Acessa o site do Google', () => {
    cy.visit('https://www.google.com');
    cy.get('input[name="q"]').type('Cypress{enter}');
  });
});
```
Rode novamente:

>npx cypress open

E selecione o arquivo exemplo.cy.js

