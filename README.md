# README - Desafio Técnico QA Júnior

## Sobre o Projeto

Este projeto foi desenvolvido como parte de um desafio técnico para a posição de **Analista de QA Júnior**.

O objetivo foi realizar uma análise funcional da plataforma **Sauce Demo**, identificando comportamentos esperados, documentando cenários de teste, registrando possíveis defeitos e propondo melhorias para a experiência do usuário.

Durante a execução dos testes foram avaliados os principais fluxos da aplicação, simulando o comportamento de um usuário em uma plataforma de e-commerce.

---

## Sistema Testado

**Aplicação:** Sauce Demo

**URL:** [https://www.saucedemo.com](https://www.saucedemo.com)

---

## Escopo dos Testes

Os testes foram realizados nos seguintes módulos:

* Login
* Validação de credenciais
* Validação de campos obrigatórios
* Listagem de produtos
* Ordenação de produtos
* Carrinho de compras
* Menu hambúrguer
* Checkout
* Checkout Overview
* Finalização de compra
* Navegação da aplicação

---

## Estratégia de Testes

Foi utilizada uma abordagem de testes manuais exploratórios e funcionais, contemplando:

### Cenários Positivos

Validação dos fluxos principais da aplicação:

* Login com sucesso
* Adição de produtos ao carrinho
* Realização de checkout
* Finalização de compra

### Cenários Negativos

Validação de regras de negócio e mensagens de erro:

* Login inválido
* Campos obrigatórios não preenchidos
* Dados inconsistentes
* Navegação incorreta

### Testes de Regressão

Validação dos comportamentos após ações como:

* Remoção de produtos
* Reset App State
* Logout
* Retorno para tela inicial

---

## Casos de Teste

Foram documentados:

* 26 Casos de Teste (CT)
* Cenários positivos
* Cenários negativos
* Regras de negócio
* Validações de interface
* Validações de cálculo

---

## Utilização de Gherkin

Além dos casos de teste tradicionais, foram criados cenários utilizando a linguagem **Gherkin**.

### Objetivo

A utilização do Gherkin teve como propósito:

* Facilitar a leitura dos cenários por pessoas técnicas e não técnicas.
* Melhorar a comunicação entre QA, Desenvolvedores e Product Owners.
* Estruturar os cenários seguindo o padrão BDD (Behavior Driven Development).
* Preparar a documentação para uma futura automação de testes.

### Exemplo

```gherkin
Feature: Login

Scenario: Login realizado com sucesso
Given que o usuário está na tela de login
When informar credenciais válidas
And clicar em Login
Then o sistema deve redirecionar para a página Products
```

Os cenários foram escritos pensando em uma futura implementação utilizando ferramentas como:

* Cucumber
* Selenium
* Cypress
* Playwright
* Robot Framework

---

## Bugs Encontrados

Durante os testes foi identificado o seguinte defeito:

### BUG-001 – Reset App State não restaura completamente o estado da aplicação

**Descrição**

Ao clicar em **Reset App State**, o contador do carrinho é zerado, porém os produtos permanecem selecionados e os botões continuam exibindo a opção **Remove**.

**Resultado Esperado**

* Limpar o carrinho.
* Restaurar os produtos para o estado inicial.
* Alterar os botões para **Add to Cart**.

---

## Melhorias Propostas

Foram identificadas oportunidades de melhoria para a aplicação:

* Exibir mensagem de sucesso após login.
* Destacar campos obrigatórios.
* Implementar exibir/ocultar senha.
* Melhorar feedback visual do carrinho.
* Exibir filtro ativo.
* Solicitar confirmação antes de Reset App State.
* Exibir número do pedido após compra.
* Implementar validação de CEP (Postal Code).

---

## Ferramentas Utilizadas

* Google Chrome
* Sauce Demo
* Microsoft Word / Google Docs
* Gherkin (BDD)

---

## Considerações Finais

Este projeto foi elaborado com foco em demonstrar conhecimentos de Qualidade de Software, documentação de testes, análise crítica de requisitos e identificação de defeitos.

Além da execução dos testes manuais, os cenários foram estruturados utilizando Gherkin visando facilitar a evolução futura para testes automatizados, seguindo boas práticas de mercado e aproximando a documentação de um ambiente real de desenvolvimento ágil.
