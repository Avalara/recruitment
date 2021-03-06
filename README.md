# Application

## Para esta etapa você deve criar um projeto node.js, usando gulp para gerenciar o projeto.

### Utilizar algum gerenciador de pacotes, como o npm;

- Faça a documentação do código no padrão do [JSDoc](http://usejsdoc.org/).

### Nesse projeto você tem que:

- *cron*: Buscar todos os Deputados Federais periodicamente. Ver [Site Deputados Federais](http://www2.camara.leg.br/deputados/pesquisa).
   - sugestão: veja [request](https://github.com/request/request) para fazer o download do HTML.
   - dica: vai precisar mudar o `User-Agent` nos teus request para de de um Browser valido.
       - veja https://github.com/request/request#custom-http-headers
       - exemplo: `'User-Agent': 'Mozilla/5.0'`
- *cron*: Fazer o parse das informações apresentadas no site, e gerar um JSON com dados.
   - sugestão: veja [jsdom](https://github.com/tmpvar/jsdom) se quiser interpretar o HTML.
- *server*: enviar o JSON com o dados para um REST no teu servidor e armazena-lo no `mongodb`.
   - POST - http://localhost:3000/api/data
   - o JSON deve ser enviado no BODY da requisição.
   - use [express](https://github.com/expressjs/express) ou [restify](https://github.com/restify/node-restify) para montar o servidor rest
- *client*: apresentar a lista de Deputados e as informações de cada Deputado numa página HTML.
- *client*: em cada item deverá ter a opção para editar a informação redirecionando para um crud do registro.

###Exemplo da estrutura do JSON esperada:

```javascript
[
  {
        "fullName": "Nome do Deputado, ex: João da Silva",
        "birthday": "Data de aniversário, formato  DD-MM",
        "party": "Sigla do Partido, ex: PJS",
        "state": "Sigla do Estado do Depudado, ex: SC",
        "main": "Se for Titular 'true', senão false ou null",
        "phone": "Telefone do Deputado Federal",
      // use a criatividade para organizar os outros dados.
  }
]
```

### Diferenciais desse projeto é a quantidade de informações que vocês consegue buscar sobre um deputado:

 - Buscar somente as **Informações do Deputado** e o **Endereço para correspondência**, não fez mais que o básico :+1: ;
 - Se bucar as **Minhas informações na Câmara** já tem um diferencial nas informações :star: ;
 - Se conseguir relacionar as informações do deputado a outro site (Facebook, LinkedIn, etc...) e complementar ainda mais o levantamento de dados, isso é além do esperado :star2: :star2: :star2:.

### Outros extras:

- [ ] Implementação de teste unitário usando [mocha](https://github.com/mochajs/mocha).
- [ ] Fazer a Análise de cobertura de código usando [istanbul](https://github.com/gotwarlost/istanbul) ou [codcov](https://codecov.io/).
- [ ] Criar gerenciador do projeto no [gulp](https://github.com/gulpjs/gulp).
- [ ] Integrar os testes do Projeto com o [travis-ci](https://travis-ci.org/).
- [ ] Integrar a cobertura de testes do Projeto com o [coveralls](https://coveralls.io/).
- [ ] Implementar a UI usando [React](https://reactjs.org/) e [Redux](http://redux.js.org/).


### Prazo para entrega é uma semana.

## Crie uma nova issue colocando no texto o link de algum projeto seu no github.
### O que vamos avaliar?

- qualidade do código
- testes
- organização

### O que não vamos avaliar?

- UX
- Arte (layout, cores e design em geral).
