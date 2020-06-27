# API Web com ASP.NET Core - CRUD completo `APIs RESTFul`

Projeto desenvolvido utilizando `ASP.NET Web API`, `Entity Framework Core` e banco de dados `SQLServer` em tempo de execução para criar `APIs RESTFul`. 

## Neste projeto foi utilizado as seguintes ferramentas para desenvolvimento:

- ASP Core 3.1
- Entity Framework Core
- SQLServer
- Visual Studio Community 2019

## Para utilizar o projeto:

Cloque o repositório para um local de sua prefenrencia. Na pasta do projeto abra um terminal de linha de comando e execute `dotnet restore` para instalar as dependências necessárias. 

Utilize o `Visual Studio Community 2019` para abrir o projeto ou solução!

## Execute o projeto:

Não tem necessidade de criar tabelas no banco de dados pois o banco de dados é usado em memória. 

Execute o projeto e utilize as solicitação abaixo para buscar, criar, deletar e atualizar os dados. 

`[HttpGet] https://localhost:44354/api/TodoItems/` - Retornam todos os dados existentes
```
Exemplo de retorno:
[
    {
        "id": 1,
        "name": "Delza",
        "isComplete": true
    },
    {
        "id": 2,
        "name": "Larisa",
        "isComplete": true
    }
]
```

`[HttpGet("{id}")] https://localhost:44354/api/TodoItems/1` - Retornam apenas um registro específico caso exista
```
Exemplo de retorno:
{
    "id": 1,
    "name": "Delza",
    "isComplete": true
}
```

`[HttpPut("{id}")] https://localhost:44354/api/TodoItems/2` - Atualiza o registro com Id 2
```
Exemplo de envio no corpo da solicitação:
  {
    "ID":2,
    "name":"feed fish",
    "isComplete":true
  }
```
`[HttpPost] https://localhost:44354/api/TodoItems/` - Salva um registro
```
Exemplo de envio no corpo da solicitação:
{
    "name": "Delza",
    "isComplete": true
}
```

`[HttpDelete("{id}")] https://localhost:44354/api/TodoItems/1` - Deleta um registro específico
```
Retorna 1 caso caso o registro seja apagado corretamente:
```
