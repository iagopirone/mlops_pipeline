# MLOps Pipeline

Projeto criado para a refatoração de um pipeline de MLOps voltado à detecção de células sanguíneas.

## Estado atual

O repositório contém a estrutura inicial do projeto e a configuração do ambiente Python com `uv`.

A implementação do pipeline será desenvolvida e refatorada nas próximas tarefas.

## Requisitos

- Git
- `uv`
- Python 3.12

As instruções de instalação do `uv` estão disponíveis na [documentação oficial](https://docs.astral.sh/uv/getting-started/installation/).

## Configuração do ambiente

Depois de clonar o repositório, acesse a pasta do projeto:

```bash
cd mlops_pipeline
```

Instale as dependências registradas no arquivo `uv.lock`:

```bash
uv sync --locked
```

O `uv` criará automaticamente o ambiente virtual `.venv` e instalará as versões exatas das dependências do projeto.

## Execução

Execute o ponto de entrada do projeto com:

```bash
uv run python main.py
```

Neste estágio inicial, o arquivo `main.py` é apenas um ponto de entrada reservado e não produz saída no terminal.

## Verificação das dependências

Para verificar se as principais dependências foram instaladas corretamente:

```bash
uv run python -c "import cv2, numpy, onnxruntime, pika, pydantic; print('Dependências carregadas com sucesso')"
```

## Testes

Os testes serão adicionados à pasta `tests` durante o desenvolvimento do projeto.

Os arquivos de teste e as funções de teste seguirão o prefixo `test_`. Quando os testes forem implementados, poderão ser executados com:

```bash
uv run pytest
```

## Gerenciamento de dependências

As dependências de execução estão declaradas no `pyproject.toml`.

As versões resolvidas de todas as dependências, inclusive as transitivas, estão registradas no `uv.lock`.