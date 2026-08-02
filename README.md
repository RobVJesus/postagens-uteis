# Postagens Úteis

Aplicativo estático (HTML + JSON) para organizar por assunto os links e textos
extraídos da conversa do WhatsApp com @R0v3rJ. Segue o mesmo padrão dos outros
projetos (Balcão de Negócios, Base de Conhecimento): `index.html` lê os dados de
um arquivo `postagens.json` publicado ao lado dele.

## Arquivos

- `index.html` — o aplicativo (também traz uma cópia dos dados embutida, usada
  somente se o `postagens.json` não puder ser carregado — por exemplo ao abrir
  o arquivo localmente sem servidor).
- `postagens.json` — os dados reais (categorias + postagens). É este arquivo
  que deve ser atualizado no repositório quando você editar conteúdos.

## Como publicar no GitHub Pages

1. Crie um repositório novo (ex.: `postagens-uteis`) em `github.com/robvjesus`,
   ou uma subpasta dentro do `robvjesus.github.io` existente.
2. Envie os dois arquivos (`index.html` e `postagens.json`) para a raiz do
   repositório (ou da subpasta).
3. Em **Settings → Pages**, habilite o GitHub Pages apontando para a branch
   `main` (pasta raiz).
4. O site ficará disponível em algo como
   `https://robvjesus.github.io/postagens-uteis/`.

## Como salvar edições feitas no site

O site é estático — ele não grava no GitHub sozinho. O fluxo de atualização é:

1. Use o site normalmente: pesquise, adicione, edite ou exclua postagens e
   categorias. Essas mudanças ficam guardadas no navegador enquanto você usa.
2. Quando quiser tornar as mudanças permanentes para todos, clique no botão
   **"JSON"** no topo da página. Isso baixa um `postagens.json` atualizado,
   já com todas as suas alterações.
3. Substitua o arquivo `postagens.json` do repositório pelo arquivo baixado
   (pelo GitHub Desktop, `git push`, ou fazendo upload direto pela interface
   web do GitHub) e faça o commit.
4. Assim que o commit for publicado, o site passará a carregar a versão
   atualizada para qualquer pessoa que o acessar.

Esse é o mesmo fluxo já usado no Balcão de Negócios (botão "Baixar JSON").
