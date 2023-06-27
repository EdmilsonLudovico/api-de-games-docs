# API de Games
  Esta API é utilizada para cadastro de Games

## Endpoints
### GET /games
Esse endpoint é responsavel por retornar a listagem de todos os games cadastrados no banco de dados.
##### Parametros
Nenhum
##### Respostas
##### Ok! 200
caso essa resposta aconteça você vai receber a listagem de todos os games.

#### Exemplo de Resposta:
```
[
    {
        "id": 23,
        "title": "Call of duty MW",
        "year": 2019,
        "price": 60
    },
    {
        "id": 65,
        "title": "Sea of thieves",
        "year": 2018,
        "price": 40
    },
    {
        "id": 2,
        "title": "Minecraft",
        "year": 2012,
        "price": 20
    }
]
```

##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autemticação da requisição. Motivos: Token inválido, Token expirado.

#### Exemplo de Resposta:
```
{
    "err": "Token inválido!"
}
```
### POST /auth
Esse endpoint é responsavel por fazer o processo de login.
##### Parametros
email: E-mail do usuário cadastrado no sistema.
Senha: Senha do usuário cadastrado no sistema.

##### Exemplo:
````
{
    "email": "edmilson.ludovico@gmail.com"
    "senha": "nodejs<3"
}
```

##### Respostas 
##### Ok! 200
caso essa resposta aconteça você receber o token JWT para acessar endpoints protegidos na API.
#### Exemplo de Resposta:
```
{
    "token": 
    yJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpZCI6MSwiZW1haWwiOiJlZG1pbHNvbi5sdWRvdmljb0BtYWlsLmNvbSIsImlhdCI6MTY4Nzg3NjcyOSwiZXhwI
    joxNjg4MDQ5NTI5fQ.zFC751Q6lc-jVvVDpLnG78krkp9VjLa27fPNMCFUbh4"
}
```
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autemticação da requisição. Motivos: Senha ou email errado.

#### Exemplo de Resposta:
```
{
    "err": "Credenciais inválido!"
}
```



