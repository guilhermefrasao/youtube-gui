---
name: descricao
description: >
  Escreve a descrição de um vídeo do canal do Guilherme Frasão pra publicar no YouTube, a partir
  do roteiro ou do tema do vídeo. Use quando o usuário pedir "escreve a descrição desse vídeo",
  "preciso da descrição pra publicar", ou depois de fechar o roteiro e a thumbnail de um vídeo.
---

# /descricao — Descrição do Vídeo

## Dependências

- **Fonte:** um roteiro em `conteudo/roteiros/` (se existir) ou o tema/ideia que o usuário der
- **Tom de voz:** a marca (`_contexto/marca/tom-de-voz.md`)
- **Contexto do negócio e público:** `_contexto/empresa.md`
- **Redes pra linkar:** `_contexto/infra.md` (canal, Instagram)

---

## Workflow

### Passo 1 — Pegar a fonte

Se o usuário apontar ou já tiver rodado `/roteiro` na sessão: usar aquele roteiro (gancho,
síntese e pilar/formato) como base. Se não tiver roteiro, perguntar do que é o vídeo antes de
escrever — não inventar conteúdo que não foi descrito.

### Passo 2 — Escrever a descrição

Estrutura:

1. **Gancho (as 2-3 primeiras linhas):** o YouTube mostra só isso antes do "mostrar mais" — tem
   que fazer sentido sozinho e dar vontade de expandir. Não repetir o título ao pé da letra.
2. **Corpo (2-4 parágrafos curtos):** do que trata o vídeo e o que a pessoa leva dele. Mesmo tom
   do roteiro — direto, honesto, sem inflar promessa.
3. **CTA:** convite pra se inscrever e seguir no Instagram (`_contexto/infra.md` tem o link).
   Sem forçar ("bora crescer junto" em vez de "não esquece de dar like e se inscrever").
4. **Links:** Instagram do Guilherme. Adicionar outros links só se o usuário pedir.

Não usar hashtag em excesso nem emoji decorativo — mesma regra de "sem poluição" do guia visual.

### Passo 3 — Calibrar contra o tom

Reler contra `_contexto/marca/tom-de-voz.md` antes de entregar: nunca promete ganho fácil ou
vida ilusória, nunca jargão ou autoridade forçada, sempre amarrado em algo real.

### Passo 4 — Salvar

Salvar em `conteudo/descricoes/AAAA-MM-DD-titulo-curto.md` (data de hoje), com o texto pronto
pra copiar e colar no YouTube Studio — sem formatação markdown dentro da descrição em si (só o
arquivo usa `.md` pra organização).

---

## Regras

- Nunca inventar conteúdo do vídeo que o usuário não descreveu
- Gancho nunca repete o título literalmente
- Sem hashtag em excesso (no máximo 3-5, só se fizer sentido) nem emoji decorativo
- CTA convida, não implora ("dar like e se inscrever, por favor" é fórmula clichê de youtuber)
