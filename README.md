# 🧪 Testes Automatizados - Central de Atendimento ao Cliente (CAC TAT)

Este projeto contém **testes automatizados end-to-end (E2E)** desenvolvidos com **Cypress**, utilizando uma aplicação de exemplo chamada **Central de Atendimento ao Cliente (CAC TAT)**.

O objetivo deste projeto é praticar e demonstrar técnicas de **automação de testes de interface**, validação de formulários e interação com elementos da página.

---

# 🚀 Tecnologias Utilizadas

* JavaScript
* Cypress
* Node.js
* HTML
* CSS

---

# 📂 Estrutura do Projeto

```
cypress-do-zero-a-nuvem
│
├── cypress
│   ├── e2e
│   │   └── cac-tat.cy.js
│   │
│   ├── fixtures
│   │   └── example.json
│   │
│   ├── support
│   │   ├── commands.js
│   │   └── e2e.js
│
├── src
│   └── index.html
│
├── cypress.config.js
├── package.json
└── README.md
```

---

# ⚙️ Instalação do Projeto

Clone o repositório:

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

Acesse a pasta do projeto:

```bash
cd cypress-do-zero-a-nuvem
```

Instale as dependências:

```bash
npm install
```

---

# ▶️ Executando os Testes

### Abrir o Cypress (modo interativo)

```bash
npx cypress open
```

### Executar testes via terminal

```bash
npx cypress run
```

---

# 🧪 Cenários de Teste Automatizados

Os testes cobrem diversas funcionalidades da aplicação:

### 📌 Validações da página

* Verificar o **título da aplicação**
* Acessar a página de **Política de Privacidade**

### 📌 Testes de formulário

* Envio do formulário com **campos obrigatórios preenchidos**
* Validação de **email inválido**
* Validação de **campos obrigatórios**
* Validação de **telefone obrigatório**

### 📌 Interação com campos

* Preenchimento e limpeza de campos
* Validação de **campo telefone apenas numérico**

### 📌 Seleção de elementos

* Seleção de produtos por:

  * texto
  * value
  * índice

### 📌 Radio buttons e checkboxes

* Seleção de tipo de atendimento
* Marcação e desmarcação de checkboxes

### 📌 Upload de arquivos

* Upload de arquivo usando:

  * caminho direto
  * drag and drop
  * fixture com alias

### 📌 Comandos customizados

Utilização de comando customizado:

```
cy.fillMandatoryFieldsAndSubmit()
```

Para simplificar o preenchimento dos campos obrigatórios do formulário.

---

# 📎 Exemplo de Teste

```javascript
it('preenche os campos obrigatórios e envia o formulário', () => {
  cy.get('[name="firstName"]').type("Melissa")
  cy.get('[name="lastName"]').type("Arantes")
  cy.get('[name="email"]').type("melissa@uol.com.br")
  cy.get('[name="open-text-area"]').type("Preciso de ajuda")
  cy.contains('.button', 'Enviar').click()

  cy.get('.success').should("be.visible")
})
```

---

# 🎯 Objetivo do Projeto

Este projeto foi desenvolvido com foco em:

* prática de **automação de testes E2E**
* uso do **Cypress**
* boas práticas de testes automatizados
* criação de **comandos customizados**
* manipulação de elementos DOM

Também serve como **projeto de portfólio para QA**.

---

# 👩‍💻 Autora

**Melissa Arantes**

* GitHub: https://github.com/melissaarantes-a11


---




