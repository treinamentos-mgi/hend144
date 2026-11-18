# 📘 Atividade: Building REST APIs with FastAPI

## 🎯 Objetivo

Construa uma API REST para gerenciar tarefas com FastAPI, praticando endpoints HTTP, validação de dados e operações CRUD. Os dados podem ser armazenados apenas em memória durante a execução do servidor.

## 📝 Tarefas

### 🛠️ Criando e executando a API

#### Descrição

Configure uma aplicação FastAPI e crie um endpoint simples para confirmar que a API está em execução.

#### Requisitos

O programa concluído deve:

- Instalar FastAPI e Uvicorn com `python -m pip install fastapi uvicorn`.
- Criar uma aplicação FastAPI no arquivo `main.py`.
- Implementar `GET /` para retornar uma resposta JSON, por exemplo `{"message": "API de tarefas ativa"}`.
- Iniciar o servidor com `uvicorn main:app --reload`.
- Disponibilizar a documentação interativa do FastAPI em `/docs`.

### 🛠️ Criando e consultando tarefas

#### Descrição

Represente tarefas como recursos da API e implemente operações para listar e criar tarefas.

#### Requisitos

O programa concluído deve:

- Definir um modelo Pydantic para os dados de uma tarefa, incluindo um título não vazio e um campo `completed` que começa como `false`.
- Armazenar tarefas em memória e atribuir um identificador único a cada tarefa durante a execução do servidor.
- Implementar `GET /tasks` para retornar a lista de tarefas, inicialmente vazia.
- Implementar `POST /tasks` para validar os dados, criar uma tarefa e responder com o status HTTP `201`.
- Retornar um erro de validação HTTP `422` quando os dados enviados forem inválidos.

Exemplo de corpo para `POST /tasks`:

```json
{
  "title": "Learn FastAPI"
}
```

Exemplo de tarefa criada:

```json
{
  "id": 1,
  "title": "Learn FastAPI",
  "completed": false
}
```

### 🛠️ Atualizando e removendo tarefas

#### Descrição

Complete as operações CRUD permitindo consultar, atualizar e remover uma tarefa pelo identificador.

#### Requisitos

O programa concluído deve:

- Implementar `GET /tasks/{task_id}` para retornar a tarefa solicitada.
- Implementar `PATCH /tasks/{task_id}` para atualizar um ou mais campos enviados, como `title` e `completed`.
- Implementar `DELETE /tasks/{task_id}` para remover a tarefa e responder com o status HTTP `204`, sem corpo de resposta.
- Responder com o status HTTP `404` quando o identificador solicitado não existir.
- Permitir testar os endpoints pela documentação interativa em `/docs`.
