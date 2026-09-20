---
name: roteiro
description: >
  Cria o roteiro de um vídeo do canal do Guilherme Frasão, a partir de um tema (do banco de
  pautas ou novo) ou de uma ideia solta. Aplica o filtro de pauta e a estrutura narrativa do
  guia editorial do canal. Use quando o usuário pedir "roteiro pro vídeo de [tema]", "bora
  escrever o roteiro", "preciso de um roteiro pra quarta/sexta", "roteiro dos 2 vídeos da
  semana", ou "vamos pensar no próximo vídeo".
---

# /roteiro — Roteiro de Vídeo

## Dependências

- **Guia editorial do canal** (pilares, filtro de pauta, formatos, banco de pautas, estrutura
  narrativa, checklist): a marca, ver mapa do `AGENTS.md` (`_contexto/marca/guia-editorial-canal.md`)
- **Tom de voz:** a marca (`_contexto/marca/tom-de-voz.md`)
- **Contexto do negócio e público:** `_contexto/empresa.md`
- **Foco atual:** `_contexto/estrategia.md`

---

## Workflow

### Passo 1 — Quantos roteiros

Perguntar se é pra escrever 1 vídeo ou os 2 da semana (o canal publica quarta e sexta). Sem
resposta clara, assumir 1 e perguntar se quer o segundo depois de entregar o primeiro.

### Passo 2 — Escolher o tema

- Se o usuário já deu um tema, ideia ou algo que aconteceu (bastidor real da semana): usar isso.
- Se não deu: olhar o banco de pautas do guia editorial e o que já foi publicado (`publicacoes/`
  e o diário recente em `_memoria/diario/`, pra não repetir tema já usado) e oferecer o próximo
  que faz sentido pro equilíbrio dos 3 formatos.

Rodar o tema pelo **filtro de pauta** do guia (aderência, experiência, tensão, utilidade,
especificidade, embalagem). Se falhar em algum critério, dizer qual antes de escrever e sugerir
um ângulo que resolva — não escrever roteiro de tema que não passou no filtro sem avisar.

Identificar o **pilar** (bastidores da construção / marketing vendas e gestão / desenvolvimento
pessoal aplicado) e o **formato** (bastidores de quem está construindo / ideias que mudam a
forma de trabalhar / marketing e negócios aplicados). Pode combinar dois pilares, desde que
tenha uma ideia central clara.

### Passo 3 — Calibrar tom

Ler `_contexto/marca/tom-de-voz.md`: direto, maduro, curioso, honesto, prático, às vezes cômico;
personagem é um empreendedor em construção, nunca um guru distante; nunca promete ganho fácil
nem vida ilusória. Ler `_contexto/empresa.md` pra lembrar o público (empreendedores, prestadores
de serviço, gestores, gente ambiciosa construindo carreira ou negócio).

### Passo 4 — Escrever o roteiro

Seguir a estrutura narrativa padrão do guia:

1. **Gancho** — a pergunta, tensão ou decisão que justifica o vídeo
2. **Contexto** — o que está acontecendo e por que importa
3. **Desenvolvimento** — o processo, os conflitos, o raciocínio
4. **Virada** — a decisão, mudança de entendimento ou consequência
5. **Síntese** — o aprendizado principal e o próximo movimento

Escrever como **rota de raciocínio** (os pontos que ele vai falar), não texto engessado pra
decorar — ele fala a partir disso, não lê pronto. Frases de transição naturais, nunca clichê de
criador de conteúdo ("e aí pessoal", "bora nessa", "não esquece de dar like e se inscrever").

No fim, incluir:

- **3 opções de título** — tensão, benefício ou curiosidade específica, nunca clickbait vazio
- **1 hipótese de thumbnail** — a tensão visual em poucas palavras (ver `_contexto/marca/design-guide.md`
  pra estilo: dark mode, contraste forte, poucos elementos)
- **Cenas reais a capturar**, se o formato for bastidores da construção

### Passo 5 — Conferir contra o checklist editorial

Antes de entregar, confirmar (checklist do guia):

- A ideia principal cabe numa frase?
- A abertura dá razão imediata pra continuar assistindo?
- Tem experiência, exemplo ou evidência real sustentando o raciocínio (não é dica genérica)?
- O final entrega uma conclusão ou mudança de perspectiva?
- Soa como o Guilherme, não uma imitação das referências do guia?

### Passo 6 — Salvar

Salvar em `conteudo/roteiros/AAAA-MM-DD-titulo-curto.md` (data de hoje, quando o roteiro foi
escrito — não a data de gravação ou publicação):

```markdown
# [título escolhido, ou as 3 opções se ainda não decidiu]

**Pilar:** ... · **Formato:** ...
**Tema:** ...

## Gancho
...

## Contexto
...

## Desenvolvimento
...

## Virada
...

## Síntese
...

## Cenas a capturar
- ...

## Hipótese de thumbnail
...
```

Se for os 2 vídeos da semana, repetir os passos 2 a 6 pro segundo, evitando repetir pilar e
formato do primeiro quando der — o guia recomenda equilíbrio entre os 3 formatos ao longo do
tempo.

---

## Regras

- Nunca fórmula de youtuber ("e aí pessoal", "não esquece de dar like e se inscrever")
- Nunca prometer ganho rápido/fácil nem vida ilusória (regra do tom de voz)
- Evitar jargão, ostentação e autoridade forçada
- Uma ideia principal por vídeo — tema amplo demais, ajudar a especificar antes de escrever
- Pedido vago ("faz um roteiro sobre produtividade") sem tema, pilar ou ângulo definido:
  perguntar antes de assumir, não inventar um ângulo genérico
