# API de Tarefas

Projeto Spring Boot em camadas `Model -> Repository -> Service -> Controller`, com JPA e banco H2.

## Requisitos

- Java 8+
- Maven 3.6+

## Execução

```bash
mvn spring-boot:run
```

A API ficará disponível em `http://localhost:8080`.

## Endpoints para o Insomnia

### Criar tarefa

`POST http://localhost:8080/api/tarefas`

```json
{
  "titulo": "Estudar Spring Boot",
  "descricao": "Revisar JPA, H2 e arquitetura em camadas",
  "concluida": false
}
```

### Listar tarefas

`GET http://localhost:8080/api/tarefas`

### Buscar tarefa

`GET http://localhost:8080/api/tarefas/1`

### Atualizar tarefa

`PUT http://localhost:8080/api/tarefas/1`

```json
{
  "titulo": "Estudar Spring Boot",
  "descricao": "Conteúdo revisado",
  "concluida": true
}
```

### Excluir tarefa

`DELETE http://localhost:8080/api/tarefas/1`

## H2 Console

Acesse `http://localhost:8080/h2-console` com:

- JDBC URL: `jdbc:h2:file:./data/tarefasdb`
- User Name: `sa`
- Password: deixe vazio

Consulta para evidência:

```sql
SELECT * FROM TAREFAS;
```

## GitHub

Depois de criar um repositório vazio no GitHub, execute:

```bash
git init
git add .
git commit -m "Implementa API de tarefas com JPA e H2"
git branch -M main
git remote add origin https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
git push -u origin main
```
