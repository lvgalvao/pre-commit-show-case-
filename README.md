# Pré Commit Show Case

Um projeto mostrando como condigura e utilizar o pre-commit

## O que é o pre-commit

O pre-commit é uma ferramenta que permite a execução de hooks antes de um commit. Esses hooks podem ser utilizados para verificar a formatação do código, a existência de arquivos grandes, a existência de arquivos com credenciais, etc.

## Como utilizar

1. Instale o pre-commit

```bash
pip install pre-commit
```

2. Crie o arquivo .pre-commit-config.yaml na raiz do projeto

```yaml
repos:
-   repo: https://github.com/pre-commit/pre-commit-hooks
    rev: v2.3.0
    hooks:
    -   id: check-yaml
    -   id: end-of-file-fixer
    -   id: trailing-whitespace
-   repo: https://github.com/psf/black
    rev: 22.10.0
    hooks:
    -   id: black
```

3. Instale os hooks

```bash
pre-commit install
```

4. Adicione os arquivos ao commit

```bash
git add .
```

5. Faça o commit

```bash
git commit -m "Adicionando pre-commit"
```

6. Veja o resultado

```bash
