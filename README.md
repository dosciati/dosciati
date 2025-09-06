# Site — Portfólio de Repositórios do GitHub (MkDocs + Actions)

Este projeto cria um **site automático** que lista seus repositórios públicos do GitHub (exclui forks) e publica no **GitHub Pages**.

## Como usar
1. Crie um repositório novo (ex.: `seu-usuario.github.io` ou `portfolio`).
2. Faça upload destes arquivos (ou extraia este ZIP na raiz do repo).
3. Em **Settings → Pages**, selecione **Source = GitHub Actions**.
4. Faça um push na `main` para disparar a Action.

## Personalize
- Edite `mkdocs.yml` (nome do site, links sociais, navegação).
- Em `docs/index.md` e `docs/contato.md`, troque `<seu-usuario>` e adicione seu conteúdo.
- **Opcional**: adicione `CNAME` com seu domínio e aponte o DNS para `<seu-usuario>.github.io`.

## Rodar localmente
```bash
pip install -r requirements.txt
mkdocs serve
```

## Como funciona
A Action usa a API do GitHub para obter todos os repositórios do **owner** deste repositório (`context.repo.owner`), gera o `docs/repos.md` e publica a pasta `site/` no Pages.

Curta e customize à vontade! 🚀