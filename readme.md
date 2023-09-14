# documentação da API

* Escolher um local do computador para criar o projeto
* Abrir o gitBash nessa pasta

Com o gitBash aberto executar o comendo para criar a raiz do projeto: (mkdir: make diretorio = criar pasta)
```
mkdir NOME_PROJETO
```

Acessar a pasta (cd = change directory)
```
cd NOME_PROJETO
```

Comando para abrir o VScode
```
code .
```

Criar o arquivo gerenciador de pacotes node (-y = yes)
```
npm init -y
```

Criar arquivo .gitignore na raiz do projeto (para não mandar arquivos para o VScode) (touch = criar arquivo)
```
touch .gitignore
```

Criar arquivo .env (arquivo para reservar variaveis do projeto)
```
touch .env
```

## Instalar os pacotes do projeto

Instalar pacotes para o projeto (i = install)
* *express*: Será o servidor da API
* *nodemon*: Atualiza os arquivos alterados sem parar o servidor
* *dotenv*: Gerenciador de variaveis de ambiente
```
npm i express nodemon dotenv
```

Criar pasta src
```
mkdir src
```

Criar arquivo server.js
```
touch src/server.js
```

Adicionar arquivos e pastas no .gitignore
```
node_modules
.env
```

Adicionar a porta do servidor no arquivo .env
```
PORT = 3000
```

Configuração básica do API com express
```
// Importar o pacote express
const express = require('express');

// Instanciar o express na variável app
const app = express();

// Recuperar o pacote dotenv
const dotenv = require('dotenv').config();

// Importando variável do arquivo .env
const PORT = process.env.PORT;

app.listen(PORT, () => console.log(`Running at port ${PORT}!`))
```

Criar comando para rodar o servidor no arquivo package.json
```
"start":"nodemon src/server.js"
```

Rodar o servidor
```
npm start
```