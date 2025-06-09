# Knowledge

Este projeto é um sistema web para gerenciar artigos de forma intuitiva e eficiente, desenvolvido utilizando Vue 2 no frontend e uma stack robusta no backend. Seu objetivo principal é fornecer uma plataforma amigável onde usuários possam criar, editar, visualizar e excluir artigos, com suporte para listagem e busca.

### Funcionalidades principais:

* Dashboard: Visão geral dos artigos cadastrados, com estatísticas de publicações.

* CRUD de Artigos: Permite criar, editar, visualizar e excluir artigos.

* Busca e Filtros: Pesquisa em tempo real e filtros por categoria.

* Editor de Texto: Ferramenta para criar conteúdo.

* Autenticação: Controle de acesso com login e logout.

### Tecnologias Utilizadas

* [Vue](https://vuejs.org/)
* [Axios](https://axios-http.com/)
* [Bootstrap-vue](https://bootstrap-vue.org/)
* [Express](https://expressjs.com/)
* [Knex](https://knexjs.org/)
* [Nodemon](https://nodemon.io/)
* [Postgresql](https://www.postgresql.org/)
* [MongoDB](https://www.mongodb.com/)

## Dependências e Versões Necessárias

* Vue - Versão: 2.5.17
* Axios - Versão: 0.18.0
* Bootstrap-vue - Versão: 2.0.0-rc.11
* Express - Versão: 4.16.3
* Knex - Versão: 0.15.2
* Nodemon - Versão: 1.18.4
* Pg - Versão: 8.0.3
* Mongoose - Versão: 5.2.17

## Como rodar o projeto ✅

### Backend

1. Acesse a pasta do backend
    ```
    cd backend
    ```
2. Instale as dependências
    ```
    npm install
    ```
3. Configure as variáveis de ambiente

    Crie um arquivo .env e configure as credenciais do banco de dados.
    Exemplo de .env:
    ```
    module.exports = {
        authSecret: '',
        db: {
            host: '127.0.0.1',
            port: 5433,
            database: 'knowledge',
            user: 'postgres',
            password: '20052406'
        }
    }
    ```
4. Rode as migrações do banco de dados relacional (PostgreSQL)
    ```
    npx knex migrate:latest
    ```
5. Inicie o servidor
    ```
    npm start
    ```

### Frontend

1. Acesse a pasta do frontend
    ```
    cd frontend
    ```
2. Instale as dependências
    ```
    npm install
    ```
3. Inicie a aplicação Vue
    ```
    npm run serve
    ```

## ⚠️ Problemas enfrentados

Este projeto requer a utilização do Node.js na versão 16 ou inferior. Isso ocorre porque algumas bibliotecas utilizadas (como o Vue 2 e o Knex) podem não ser compatíveis com versões mais recentes do Node, como a 18 ou a 20, o que pode gerar erros de instalação ou de execução.

Portanto, antes de instalar e rodar o projeto, verifique sua versão do Node.js com o comando:
```
node -v
```
Caso esteja utilizando uma versão superior à 16, recomendamos trocar para a versão 16 ou inferior. Uma forma prática de gerenciar versões do Node é utilizando o nvm (Node Version Manager):
```
nvm install 16
nvm use 16
```

Dessa forma, você garante que a aplicação funcione corretamente e evita possíveis erros de compatibilidade durante a instalação das dependências ou na execução do servidor.