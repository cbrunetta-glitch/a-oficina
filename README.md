# A Oficina

Ambiente único onde residem as quatro ferramentas pedagógicas para o
refinamento da pesquisa acadêmica, para mestrandos, doutorandos e professores do
PPGD/FADISP. Nasceram no Seminário de Pesquisa e hoje servem ao Programa inteiro
(descrição revista pela Profª Cíntia Brunetta em 29/09/2026):

| Porta | App | Endereço |
|---|---|---|
| 1ª | O Interrogador | https://ointerrogadorfadisp.com |
| 2ª | O Alinhador | https://oalinhadorfadisp.com |
| 3ª | O Arquiteto | https://oarquitetofadisp.com |
| 4ª | O Parecerista | https://opareceristafadisp.com |

A ordem dos cards é a ordem do trabalho: interrogar a pesquisa → alinhar a
cadeia → desenhar o método → ser lido.

**A ordem é regra da disciplina, não arranjo visual** (Profª Cíntia Brunetta,
22/08/2026):

- o **Interrogador** vem primeiro porque interroga a própria pesquisa — pergunta,
  hipótese, lacuna a preencher, referenciais teóricos;
- o **Alinhador** vem depois: ele confere se as peças encaixam entre si, o que
  pressupõe peças com substância;
- o **Arquiteto** só entra aí, porque **o método obedece à pergunta, não ao
  pesquisador** — sem clareza e refinamento da pergunta e da hipótese não há o
  que desenhar;
- o **Parecerista** fecha, lendo o que já virou texto.

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

## Identidade visual

Desde 29/09/2026 segue a do Élis (https://mestradoedoutorado.alfa.br): faixa
vermelha `#D92322` com a marca ALFA Escola de Direito em branco
(`logo-alfa-branco.png`, a mesma usada pela Goiandira), fundo cinza-claro,
cartões brancos arredondados e botões pretos. Os sistemas da Escola de Direito
se leem como um conjunto.
