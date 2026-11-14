# IST Docs Portal

Portal público de documentação institucional da Info Service Technology.

## Desenvolvimento local

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
mkdocs serve
```

## Verificação

```bash
mkdocs build --strict
```

## Publicação

Após aprovação da publicação, configurar **Settings > Pages > Build and deployment > Source: GitHub Actions**. O workflow `pages.yml` possui apenas execução manual (`workflow_dispatch`). Não há publicação automática por push.

**Atenção:** a publicação exige autorização explícita e configuração do GitHub Pages. Antes de disponibilizar qualquer conteúdo, revisar privacidade e segurança.
