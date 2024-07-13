# Desafio-API_FastAPI

API com FastAPI - DIO ( https://web.dio.me/play ) para 'Desenvolvedor de backend Python AI'

API rápida
Quem é o FastAPi?
Framework FastAPI, alta performance, fácil de aprender, fácil de programar, pronto para produção. FastAPI é um framework web moderno e rápido (de alta performance) para construção de APIs com Python 3.6 ou superior, baseado nos padrões type hints do Python.

Assíncrono
Código assíncrono significa apenas que a linguagem tem um jeito de dizer para o computador / programa que em certo ponto, ele terá que esperar por algo para finalizar em outro lugar

Projeto
API de treino
Esta é uma API de competição de crossfit chamada WorkoutAPI (isso mesmo rs, eu acabei unificando duas coisas que gosto: codar e treinar). É uma API pequena, pois será um projeto mais prático e simplificado, pois desenvolveremos uma API de poucas tabelas, mas com o necessário para você aprender como utilizar o FastAPI.

Modelagem de entidade e relacionamento - MER
MAIS

Pilha da API
A API foi desenvolvida utilizando o fastapi(async), juntamente com as seguintes bibliotecas: alembic, SQLAlchemy, pydantic. Para salvar os dados está sendo utilizado o postgres, por meio do docker.

Execução da API
Para executar o projeto, utilizei o pyenv , com a versão 3.11.4 do pythonambiente virtual.

Caso opte por usar pyenv, após instalar, execute:

pyenv virtualenv 3.11.4 workoutapi
pyenv activate workoutapi
pip install -r requirements.txt

Para subir o banco de dados, caso o docker-compose não tenha sido instalado, faça a instalação e logo em seguida, execute:

make run-docker
Para criar uma nova migração, execute:

make create-migrations d="nome_da_migration"
Para criar o banco de dados, execute:

make run-migrations
API
Para subir a API, execute:

make run
e acesse: http://127.0.0.1:8000/docs

Desafio Final

- adicionar query parameters nos endpoints
  - atleta
    - nome
    - cpf
- customizar response de retorno de endpoints
  - get all
    - atleta
      - nome
      - centro_treinamento
      - categoria
- Manipular exceção de integridade dos dados em cada módulo/tabela
  - sqlalchemy.exc.IntegrityError e devolver a seguinte mensagem: “Já existe um atleta cadastrado com o cpf: x”
  - status_code: 303
- Adicionar paginação utilizando a lib: fastapi-pagination - limit e offset
  Referências
  FastAPI: https://fastapi.tiangolo.com/

Pydantic: https://docs.pydantic.dev/latest/

SQLAlchemy: https://docs.sqlalchemy.org/en/20/

Alembic: https://alembic.sqlalchemy.org/en/latest/

Paginação Fastapi: https://uriyyo-fastapi-pagination.netlify.app/
