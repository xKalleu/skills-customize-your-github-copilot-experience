# 📘 Atividade: APIs REST com FastAPI

## 🎯 Objetivo

Construa uma API REST para cadastrar e consultar livros usando FastAPI. Você praticará rotas HTTP, validação de dados e respostas JSON, mantendo os dados em memória.

## 📝 Tarefas

### 🛠️ Criar e executar sua primeira rota

#### Descrição
Comece com uma aplicação pequena: crie um ambiente virtual, instale o FastAPI e escreva um arquivo `main.py` com uma instância chamada `app`. Reserve cerca de 10 minutos para colocar sua primeira rota em funcionamento.

Use estes comandos no terminal:

```bash
python -m venv .venv
```

Ative o ambiente com `source .venv/bin/activate` no Linux/macOS ou `.venv\Scripts\Activate.ps1` no PowerShell. Depois, instale e execute:

```bash
python -m pip install "fastapi[standard]"
fastapi dev main.py
```

#### Requisitos
O programa concluído deve:

- Iniciar localmente em `http://127.0.0.1:8000`.
- Disponibilizar `GET /` com status `200` e o JSON `{"message": "API de livros"}`.
- Exibir a documentação interativa em `/docs`.
- Permitir testar a rota inicial pelo botão **Try it out** da documentação.

### 🛠️ Cadastrar e listar livros

#### Descrição
Adicione as rotas de criação e listagem de livros. Use um modelo Pydantic para validar a entrada e uma lista em memória para armazenar os registros; não é necessário configurar banco de dados.

Exemplo de entrada para `POST /books`:

```json
{
  "title": "O Pequeno Principe",
  "author": "Antoine de Saint-Exupery"
}
```

Exemplo de resposta para o primeiro cadastro:

```json
{
  "id": 1,
  "title": "O Pequeno Principe",
  "author": "Antoine de Saint-Exupery"
}
```

#### Requisitos
O programa concluído deve:

- Implementar `POST /books` com status `201` e retornar o livro criado.
- Exigir `title` e `author` como strings com pelo menos um caractere.
- Gerar um identificador inteiro único para cada livro.
- Implementar `GET /books` com status `200`, retornando uma lista JSON de todos os livros.
- Retornar uma lista vazia quando não houver livros cadastrados.
- Retornar status `422` quando campos obrigatórios estiverem ausentes ou vazios.
- Manter os livros disponíveis durante a execução; os dados podem ser perdidos ao reiniciar a aplicação.

### 🛠️ Consultar um livro e verificar as respostas

#### Descrição
Implemente a consulta de um livro pelo identificador e trate os casos em que ele não existe. Use `/docs` para verificar os cenários e registre os resultados em um arquivo `test-results.txt`.

#### Requisitos
O programa concluído deve:

- Implementar `GET /books/{book_id}` com um parâmetro inteiro.
- Retornar status `200` e o livro completo quando o identificador existir.
- Retornar status `404` com `{"detail": "Livro nao encontrado"}` quando o identificador não existir.
- Retornar status `422` quando o identificador não for um inteiro.
- Registrar método, caminho, entrada quando aplicável, status esperado e status observado para seis cenários: listagem vazia, cadastro válido, listagem após cadastro, consulta existente, consulta inexistente e cadastro inválido.
