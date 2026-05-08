# Euro Colchões · UI Kit

Sistema visual da Euro Colchões em HTML standalone. Cobre Foundation (cores, tipografia, espaçamento, raios, sombras, grid), componentes (botões, selos, ícones, formulários, card de produto, filtros, tabela comparativa, selos de confiança), Landing Page (hero, prova social, FAQ, countdown) e diretrizes (CTA, fotografia, performance).

## Estrutura

```
uikit/
├── uikit-euro-colchoes.html   ← arquivo principal
├── vercel.json                ← config de hosting
├── README.md
└── assets/
    ├── favicon-32.png · favicon-64.png · favicon-256.png · apple-touch-icon.png
    ├── logo-euro-white.png
    ├── hero-1.jpg · hero-3.jpg   ← backgrounds desfocados
    ├── foto-vermelha.jpg          ← referência fotografia vermelha
    └── produto-1.png              ← Box com Baú Corano Areia
```

Arquivo 100% standalone: nada de CDN, npm, build. Abre direto no navegador.

## Deploy no Vercel

### Caminho A · Drag & drop (recomendado, ~60s)

1. Acesse [vercel.com](https://vercel.com) e logue.
2. No dashboard: **Add New → Project → Upload**.
3. Arraste a pasta `uikit/` inteira.
4. Clique **Deploy**. Em ~30s sai a URL pública.

### Caminho B · CLI

```bash
npm i -g vercel
cd /caminho/para/uikit
vercel --prod
```

## Hospedando

O `vercel.json` faz três coisas:

- `rewrites` mapeia `/` para `uikit-euro-colchoes.html`, então a URL pública carrega direto sem precisar do nome longo
- `cleanUrls: true` remove extensões `.html` da URL
- Cache de 1 ano para tudo em `/assets/` (imagens não voltam pro servidor)

## Domínio próprio

Após o deploy, em **Settings → Domains** do projeto Vercel, adicione um subdomínio personalizado (ex: `uikit.eurocolchoes.com.br`). Vercel emite SSL automaticamente.

## Atualizando

Editou o HTML ou trocou alguma imagem? Reupload pelo dashboard (mesmo projeto, "Redeploy") ou rode `vercel --prod` de novo. Cache em `assets/` é invalidado automaticamente quando o arquivo muda.

## Versão

UI Kit v0.2 · 2026-05-08 · DM Serif Display + Roboto · paleta `#AC2629` / `#344D66`
