---
name: thumbnail
description: >
  Cria a thumbnail de um vídeo do canal do Guilherme Frasão: monta um HTML na identidade visual
  do canal e renderiza em PNG (1280x720, padrão YouTube) via Playwright. Use quando o usuário
  pedir "faz a thumbnail", "cria a capa do vídeo", "preciso da thumb desse roteiro", ou depois
  de fechar um roteiro com `/roteiro`.
---

# /thumbnail — Thumbnail do Vídeo

> Versão simples (template renderizado), combinada com o Guilherme em 2026-09-20: quando ele
> tiver mais tempo pra algo mais elaborado (foto, composição, Canva manual), essa skill se ajusta.

## Dependências

- **Template:** `template.html`, nesta mesma pasta (1280x720, fundo preto, título branco com
  destaque em laranja, fonte Space Grotesk — vem de `_contexto/marca/design-guide.md`)
- **Checklist de embalagem:** a marca, ver mapa do `AGENTS.md` (`_contexto/marca/guia-editorial-canal.md`)
- **Playwright:** já instalado (chromium). Se faltar num computador novo: `npx playwright install chromium`

---

## Workflow

### Passo 1 — Pegar o texto da thumbnail

Se veio de um roteiro (`/roteiro` acabou de rodar, ou o usuário aponta um arquivo em
`conteudo/roteiros/`): usar a "Hipótese de thumbnail" e os títulos sugeridos de lá como ponto de
partida.

Se não: perguntar "qual é o texto da thumbnail?" — curto, poucas palavras (o guia pede: adiciona
informação em vez de repetir o título, tensão visual clara).

Perguntar (ou sugerir) qual palavra ou trecho curto merece o destaque em laranja — normalmente a
palavra que carrega a tensão ou o benefício (ex: "o erro que **trava** todo mundo").

### Passo 2 — Montar o HTML

Copiar `template.html` pra um arquivo temporário e substituir:

- `{{HANDLE}}` → `@guilherme.frasao`
- `{{TITULO_HTML}}` → o texto, com a palavra/trecho de destaque envolto em `<span class="d">...</span>`

Regra de tamanho: o template já ajusta a fonte pra caber, mas texto muito longo (mais de ~6-7
palavras) fica ilegível numa thumbnail — se o texto for grande, ajudar a cortar pro essencial
antes de renderizar. Não deixar nada crítico no canto inferior direito (o YouTube cobre essa
área com a duração do vídeo).

### Passo 3 — Renderizar

```bash
npx playwright screenshot --viewport-size=1280,720 "file:///caminho/absoluto/temp.html" "conteudo/thumbnails/AAAA-MM-DD-titulo-curto.png"
```

Usar a data de hoje (quando a thumbnail foi criada) e um título curto batendo com o roteiro,
quando houver.

### Passo 4 — Mostrar e confirmar

Mostrar a imagem gerada (Read do PNG) antes de dar por encerrado. Perguntar se o texto, o
destaque ou o tamanho da fonte precisam de ajuste — se sim, editar e renderizar de novo.

---

## Regras

- Sempre 1280x720 (padrão de thumbnail do YouTube)
- Só um destaque em laranja por thumbnail — mais que isso perde a força
- Texto curto sempre: a thumbnail se lê em menos de 1 segundo
- Nada de emoji nem de moldura/seta genérica de "youtuber" — a identidade do canal é clean, sem
  poluição
- Apagar o HTML temporário depois de renderizar (só o PNG final fica em `conteudo/thumbnails/`)
