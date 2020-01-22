# americanas-cypress
Automação com Cypress v.3.7.0 (https://www.cypress.io/)

Como executar o projeto:

1. Realizar o download do projeto para alguma pasta do seu computador, exemplo "C:\" e descompactar o arquivo.

2. Acessar a pasta do projeto:
C:\Cypress-Americanas-Test

3. Abrir o cypress, executar pelo prompt:
npx cypress open

4. Com o Cypress Server aberto, executar o arquivo na aba "</> Tests > Integration Tests":
cadastro-spec.js
___

Organização do projeto:

Spec:
cypress\integration > cadastro-spec.js

Page Object:
cypress\support\pages > login-po.js 
cypress\support\pages > cadastro-po.js
___

O que consegui executar:
- Acessar a página Americanas.com.br
- Acessar a página de cadastro
- Informar os campos
- Validar máscara correta nos campos
- Validar a mensagen de Senha Fraca 
- Clique no botão "criar seu cadastro"

Anexo: C:\Cypress-Americanas-Test\execucao-spec-falha.png

O que não consegui executar:
- Finalizar o cadastro inválido
- Cadastro efetuado com sucesso
- Busca pelo texto "Moto G6"
- Adicionar dois produtos na cesta
- Validar que o total da compra é inferior a 5 mil reais
- Validar que a compra pode ser dividida em até 10x sem juros

Dificuldades - Finalizar o cadastro inválido:
1. Para garantir a mensagem de "E-mail já cadastrado" é necessário o clique no botão "criar seu cadastro".
Tentei de várias formas capturar o elemento do re-Captcha e o ignorar dando o clique no botão "ESC", porém sem sucesso.

2. Para validar a mensagem de "CPF inválido" não consegui reproduzir o cenário de forma manual, este cenário também deveria ocorrer após o clique no botão "criar seu cadastro", porém ele não retornou.
Anexo: C:\Cypress-Americanas-Test\cpf-invalido-nao-retorna.png












