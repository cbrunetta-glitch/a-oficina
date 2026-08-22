# A Oficina

Ambiente único onde residem as quatro ferramentas pedagógicas do Seminário de
Pesquisa (PPGD/FADISP):

| Porta | App | Endereço |
|---|---|---|
| 1ª | O Arquiteto | https://oarquitetofadisp.com |
| 2ª | O Alinhador | https://oalinhadorfadisp.com |
| 3ª | O Interrogador | https://ointerrogadorfadisp.com |
| 4ª | O Parecerista | https://opareceristafadisp.com |

A ordem dos cards é a ordem do trabalho: desenhar → alinhar → aguentar a
pergunta → ser lido.

## Estrutura

- `index.html` — a página inteira (HTML + CSS, sem JS, sem build, sem banco)

Não há função serverless: a Oficina não fala com a API da Anthropic. Ela é a
fachada; quem chama a API é cada um dos quatro apps.

## Deploy

Projeto `a-oficina` na Vercel (time `cbrunetta-2386s-projects`), raiz do repo
como raiz do projeto. **Sem `vercel.json`** — ele conflita com o roteamento
automático, mesma lição do Alinhador.

Domínio: `aoficinafadisp.com.br`, registrado no Registro.br. Apontar **apex e
`www`** — o `www.oalinhadorfadisp.com` ficou fora do ar por não ter sido
adicionado.

Qualquer alteração precisa de commit + push; a Vercel redeploya sozinha.

## Onde a Oficina se encaixa

- **Élis** (https://mestradoedoutorado.alfa.br/aluno/login) é o portal
  administrativo do aluno: bancas, créditos, tira-dúvidas, guias.
- **A Oficina** é o ambiente de pesquisa. O Élis aponta para cá com **um** link,
  em vez de quatro.

Próximos passos previstos (ainda não implementados): identidade única por
matrícula via Supabase, painel único da professora, e a pesquisa como objeto
compartilhado entre as quatro ferramentas.
