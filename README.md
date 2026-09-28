### Exercícios

1. **401, 403 ou cache: qual se aplica?** — check rápido identificando o status code/cabeçalho correto para quatro cenários dados.
2. **Construindo um endpoint de listagem e criação** — implementar `GET` e `POST` em `TarefaController`, com `TarefaService`, testando com curl/Postman.
3. **Completando o CRUD de `/tarefas`** — adicionar `GET /{id}` e `DELETE /{id}`, `TarefaDTO` com validação, `ResponseEntity` com `204 No Content`, e um `@RestControllerAdvice` para a exceção de tarefa não encontrada.

Solução de referência dos Exercícios 2 e 3 em [`exemplo_tarefas`](<Aula 07/exemplo_tarefas>):

```bash
cd "Aula 07/exemplo_tarefas"
mvn spring-boot:run

# abra http://localhost:8080/ no navegador para usar a página de cadastro
# (chama a API de verdade e loga cada passo), ou teste direto por curl:
curl http://localhost:8080/tarefas
curl -X POST http://localhost:8080/tarefas -H "Content-Type: application/json" -d '{"titulo":"Estudar Spring Web"}'
curl http://localhost:8080/tarefas/1
curl -X DELETE http://localhost:8080/tarefas/1
```

---
