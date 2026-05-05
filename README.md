# Dashboard — Proposta 4: Agropecuária comparada

Dashboard interativo em HTML, CSS e JavaScript puro para o trabalho da Proposta 4.

## O que o painel faz

- Compara Brasil, Estados Unidos, China, Japão e Índia.
- Permite selecionar vários países ao mesmo tempo.
- Mostra séries anuais de produção agropecuária por produto.
- Exibe tabela de dados brutos filtrados.
- Permite baixar os dados filtrados em CSV.
- Tem campo editável para o nome do grupo.
- Tem área para importar dados complementares de valor agregado, exportação, destino e dependência de mercado.

## Arquivos

- `index.html`: dashboard principal. É o arquivo que o GitHub Pages abre como página inicial.
- `dados_complementares_modelo.csv`: modelo para preencher valor agregado, exportação e destinos.
- `.nojekyll`: evita processamento por Jekyll no GitHub Pages.

## Como abrir no computador

1. Baixe esta pasta.
2. Abra o arquivo `index.html` no navegador.
3. Edite o campo "Nome do grupo" no cabeçalho.
4. Use os filtros de país, produto, categoria e intervalo de anos.

## Como subir no GitHub

### Opção 1 — pelo site do GitHub

1. Crie um repositório novo no GitHub.
2. Faça upload dos arquivos desta pasta: `index.html`, `dados_complementares_modelo.csv`, `.nojekyll` e `README.md`.
3. Vá em **Settings > Pages**.
4. Em **Build and deployment**, escolha **Deploy from a branch**.
5. Em **Branch**, selecione `main` e a pasta `/root`.
6. Clique em **Save**.
7. Depois de alguns instantes, o site ficará disponível em uma URL parecida com:
   `https://seu-usuario.github.io/nome-do-repositorio/`

### Opção 2 — pelo Git no computador

```bash
git init
git add .
git commit -m "Adiciona dashboard da proposta 4"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/NOME-DO-REPOSITORIO.git
git push -u origin main
```

Depois disso, ative o GitHub Pages em **Settings > Pages**.

## Como editar o nome do grupo

No próprio dashboard, altere o campo no cabeçalho.

Se quiser deixar fixo no código, abra `index.html`, procure por:

```html
<input id="groupName"
```

e altere o valor dentro de `value="..."`.

## Como atualizar os dados complementares

Use o arquivo `dados_complementares_modelo.csv` como base. As colunas são:

```csv
ano,pais,produto,categoria,valor_bi_usd,exportacao_pct,principal_destino,destino_pct,risco,observacao
```

Depois de preencher, abra o dashboard, cole o CSV na área de importação e clique em **Importar dados complementares**.

## Fontes sugeridas

- FAOSTAT: produção agropecuária internacional.
- Our World in Data Grapher: API CSV derivada de FAOSTAT.
- IBGE/SIDRA: produção agropecuária brasileira.
- MAPA AgroStat: exportações do agronegócio brasileiro.
- Comex Stat/UN Comtrade: comércio exterior e destinos das exportações.
