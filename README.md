# crud-todo-nodejs
Aplicação para gerenciar tarefas desenvolvida com NodeJs;

### Execução da aplicação
1. Após clonar o repositório, na pasta src, execute `yarn` para baixar as dependências. 
2. Feito isso, execute o comando `yarn dev`para rodar a aplicação.

#### Execução dos testes
Para rodar os testes, execute `yarn test`

### Rotas da aplicação

**POST/**`users` - criar um novo usuário

request.body:
```
{ 
	name: 'Antonia Luciana Pires', 
	username: 'antonia'
} 
```

**POST/**`todos` - criar nova tarefa 

**header:** username = antonia

request.body:
```
{ 
	"title": "Nome da tarefa",
	"deadline": "2021-02-27"
} 
```

**GET/**`todos` - consultar tarefas do usuário

**header:** username = antonia

response.body:
```
[
  { 
    "id": "b43dcb4d-f7a1-494c-95a7-f66bff52bbfd", 
    "title": "Nome da tarefa",
    "done": false, 
    "deadline": "2021-02-27T00:00:00.000Z", 
    "created_at": "2021-02-22T00:00:00.000Z"
  }
]
```

**PUT/**`todos/:id` - atualizar tarefa

**header:** username = antonia

request.body:
```
{ 
	"title": "Nome da tarefa atualizada",
	"deadline": "2021-02-27"
} 
```

**PATCH/**`todos/:id/done` - concluir tarefa

**header:** username = antonia
```
{ 
    "id": "b43dcb4d-f7a1-494c-95a7-f66bff52bbfd", 
    "title": "Nome da tarefa atualizada",
    "done": true, 
    "deadline": "2021-02-27T00:00:00.000Z", 
    "created_at": "2021-02-22T00:00:00.000Z"
  }
```

**DELETE/**`todos/:id` - deletar tarefa
