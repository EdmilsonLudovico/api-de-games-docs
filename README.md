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
##### Falha na autenticação! 401
Caso essa resposta aconteça, isso significa que aconteceu alguma falha durante o processo de autemticação da requisição. Motivos: Token inválido, Token expirado.

