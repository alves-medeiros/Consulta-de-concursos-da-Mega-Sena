# Consulta de Concursos da Mega-Sena

## 📋 Descrição

Aplicação desenvolvida em **Node.js** utilizando o framework **Express** para consulta de resultados da Mega-Sena.

O sistema utiliza uma base local de dados armazenada em **PostgreSQL**, alimentada a partir de um arquivo CSV contendo o histórico de concursos da Mega-Sena. Os dados foram obtidos através do portal oficial das Loterias CAIXA.

A aplicação disponibiliza uma interface web simples que permite:

* Consultar o último concurso realizado;
* Buscar concursos específicos pelo número do concurso;
* Visualizar as dezenas sorteadas;
* Consultar a data do sorteio;
* Verificar informações de premiação;
* Visualizar a estimativa do próximo prêmio.

## 🏗️ Arquitetura

O projeto é composto pelos seguintes componentes:

### Backend

* Node.js
* Express
* PostgreSQL

### Frontend

* HTML
* CSS
* JavaScript

### Banco de Dados

* PostgreSQL
* Importação de dados via arquivo CSV

## 📊 Fonte dos Dados

Os resultados da Mega-Sena utilizados neste projeto foram obtidos a partir do portal oficial da CAIXA:

https://loterias.caixa.gov.br/Paginas/Mega-Sena.aspx

Os dados são armazenados localmente em banco de dados PostgreSQL para permitir consultas rápidas e independentes de serviços externos.

## 🚀 Funcionalidades

### Consultar Último Concurso

Permite visualizar automaticamente o concurso mais recente disponível na base de dados.

### Buscar Concurso por Número

Permite informar o número de um concurso específico e consultar suas informações.

### Exibição de Resultados

Para cada concurso são exibidos:

* Número do concurso;
* Data do sorteio;
* Dezenas sorteadas;
* Informações de premiação;
* Estimativa do prêmio do próximo concurso.

## 📁 Estrutura do Projeto

```text
project/
│
├── src/
│   ├── controllers/
│   ├── routes/
│   ├── services/
│   ├── database/
│   └── app.js
│
├── public/
│   ├── css/
│   ├── js/
│   └── index.html
│
├── data/
│   └── mega_sena.csv
│
├── package.json
└── README.md
```

## ⚙️ Instalação

### Pré-requisitos

* Node.js (versão 18 ou superior)
* PostgreSQL
* npm

### Clonando o projeto

```bash
git clone <url-do-repositorio>
cd <nome-do-projeto>
```

### Instalando dependências

```bash
npm install
```

### Configurando o banco de dados

Crie um banco PostgreSQL e configure as credenciais de acesso em um arquivo `.env`.

Exemplo:

```env
DB_HOST=localhost
DB_PORT=5432
DB_NAME=mega_sena
DB_USER=postgres
DB_PASSWORD=senha
```

### Importando os dados

Execute o script responsável pela leitura do arquivo CSV e carga dos dados no PostgreSQL.

```bash
npm run import
```

### Executando a aplicação

```bash
npm start
```

A aplicação estará disponível em:

```text

```

## 📡 Endpoints

### Buscar último concurso

```http
GET /api/concursos/ultimo
```

### Buscar concurso por número

```http
GET /api/concursos/:numero
```

Exemplo:

```http
GET /api/concursos/2800
```

## 💻 Interface Web

A interface web consome os endpoints disponibilizados pelo servidor Express e apresenta os dados de forma amigável ao usuário.

As consultas são realizadas via requisições HTTP assíncronas, permitindo a atualização dos resultados sem necessidade de recarregar a página.

## 🎯 Objetivo Educacional

Este projeto foi desenvolvido com fins educacionais para demonstrar conceitos de:

* Desenvolvimento Web com Node.js e Express;
* Integração com banco de dados PostgreSQL;
* Importação e tratamento de arquivos CSV;
* Criação de APIs REST;
* Consumo de APIs via JavaScript no frontend;
* Manipulação e exibição de dados em páginas web.

## 📄 Licença

Este projeto é destinado para fins acadêmicos e educacionais.

Os dados utilizados pertencem à CAIXA Econômica Federal e são disponibilizados publicamente através do portal oficial das Loterias CAIXA.
