# Exercício de Teste de API com Postman

Projeto desenvolvido com o objetivo de praticar testes automatizados de API utilizando o Postman.

O repositório contém coleções, validações e testes automatizados de endpoints REST, simulando cenários comuns encontrados em aplicações reais.

Repositório:

[GitHub - Exercício de Teste de API com Postman](https://github.com/Noobdub55/exexrcicio-de-teste-de-API-com-postman?utm_source=chatgpt.com)

---

# Objetivo do Projeto

O objetivo deste projeto é demonstrar conhecimentos em:

- Testes de API REST
- Validação de respostas HTTP
- Estruturação de coleções no Postman
- Automação de testes
- Organização de requisições
- Versionamento com GitHub

---

# Tecnologias Utilizadas

- Postman
- Newman
- Node.js
- GitHub

---

# Estrutura do Projeto

```bash
exexrcicio-de-teste-de-API-com-postman/
│
├── collections/
│   └── colecao_testes.json
│
├── environments/
│   └── ambiente.json
│
├── README.md
└── package.json
```

---

# Funcionalidades Testadas

Os testes realizados validam:

- Status Code das requisições
- Tempo de resposta da API
- Estrutura do JSON retornado
- Campos obrigatórios
- Validação de dados retornados
- Métodos HTTP
  - GET
  - POST
  - PUT
  - DELETE

---

# Exemplos de Validações

## Validação de Status Code

```javascript
pm.test("Status code é 200", function () {
    pm.response.to.have.status(200);
});
```

---

## Validação de Tempo de Resposta

```javascript
pm.test("Tempo de resposta menor que 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});
```

---

## Validação de Campo no JSON

```javascript
pm.test("Resposta contém o campo id", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.have.property("id");
});
```

---

# Como Executar o Projeto

## 1. Instalar dependências

```bash
npm install
```

---

## 2. Executar os testes via Newman

```bash
npx newman run collections/colecao_testes.json
```

---

# Execução pelo Postman

1. Abra o Postman
2. Importe a collection do projeto
3. Importe o environment
4. Execute as requisições manualmente ou utilizando o Collection Runner

---

# Objetivos de Aprendizado

Durante o desenvolvimento deste projeto foram praticados:

- Estruturação de testes automatizados
- Manipulação de APIs REST
- Criação de assertions
- Organização de collections
- Testes de integração
- Automação com Newman

---

# Boas Práticas Aplicadas

- Separação de ambientes
- Organização das collections
- Uso de assertions reutilizáveis
- Estrutura limpa e legível
- Versionamento do projeto no GitHub

---

# Referências

- [Postman Official Website](https://www.postman.com/?utm_source=chatgpt.com)
- [Newman Documentation](https://www.npmjs.com/package/newman?utm_source=chatgpt.com)
- [Postman Learning Center](https://learning.postman.com/?utm_source=chatgpt.com)

---

# Autor

Matheus Lima de Aquino
