O ano é 2100 e a 3CPlus decidiu expandir seus negócios para espaço, então precisamos de uma plataforma para cadastrar galaxias e os planetas que fazem parte dela.

## Requisitos

Sinta-se livre para fazer qualquer um dos próximos requisitos diferente do que foi pedido desde que consiga justificar a mudança. Ex.: não fiz o requisito de tal maneira pois a implementação que eu fiz é mais performática e segura.

- Utilize docker-compose, que simplifique rodar o seu servidor e o DB
- Documente o seu projeto, e explique como rodar ele
- Crie o projeto em algum repositório privado no GitHub

### Laravel
Primeiro voce deve criar uma API Rest JSON utilizando laravel para cadastrar uma galáxia e que também seja possível adicionar planetas nela. Pode utilizar qualquer banco de dados que desejar (Aqui na 3CPlus usamos Postgres e MongoDB).

- **POST** /galaxies

Exemplo de json para cadastro.
```json
{
   "name":"Milky Way",
   "radius":9.46073e+20,
   "mass":1.153678e+42
}
 ```
 
- **POST** /planets

Exemplo de json para cadastro.
```json
{
   "planet":"Earth",
   "moons":1,
   "diameter":12756,
   "galaxy_id":1
}
```
  
- **GET** /galaxies/{galaxy-id}

Exemplo de json de retorno.
```json
{
   "name":"Milky Way",
   "radius":9.46073e+20,
   "mass":1.153678e+42,
   "planets":[
      {
         "planet":"Earth",
         "moons":1,
         "diameter":12756,
         "galaxy_id":1
      },
      {
         "planet":"Venus",
         "moons":0,
         "diameter":12104,
         "galaxy_id":1
      }
   ]
}
```
### Vue.js
Agora você deverá consumir a API utilizando [Vue.js](https://vuejs.org/) para isso você deverá criar uma tela inicial que exiba todas as galaxias e ao clicar em uma galaxia irá exibir os dados dela e seus planetas. 

# Extras

- Adicione testes usando PHPUnit
- Utilizar phplint e eslint.
- Adicione autenticação.
