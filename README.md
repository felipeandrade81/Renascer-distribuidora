# Sistema RENASCER no GitHub Pages

Este conteúdo é uma página única (`index.html`), sem servidor e sem instalar nada.
O GitHub Pages só mostra o site quando existe um arquivo chamado **exatamente `index.html`** na raiz do que foi publicado.
O erro "404 · File not found" que você viu significa que esse arquivo não foi encontrado.

## Passo a passo

1. Em **github.com**, clique em **New repository**. Dê um nome (ex.: `renascer`), marque **Public** e clique em **Create repository**.
2. Na página do repositório, clique em **uploading an existing file** (ou *Add file › Upload files*).
3. Arraste para lá **os arquivos** (não a pasta): `index.html`, `404.html` e `.nojekyll`. Eles precisam ficar **na raiz**, fora de qualquer pasta.
   Se o computador esconder o `.nojekyll` (arquivo que começa com ponto), pode subir sem ele: ele é opcional.
4. Clique em **Commit changes**.
5. Vá em **Settings › Pages**. Em *Build and deployment*, escolha **Source: Deploy from a branch**, **Branch: `main`** e a pasta **`/ (root)`**. Clique em **Save**.
6. Espere 1 a 3 minutos e atualize. O endereço aparece no topo da mesma tela:
   `https://SEU-USUARIO.github.io/renascer/`
   (a barra no final importa). Se quiser, marque **Enforce HTTPS**.

## Se ainda aparecer o 404

- O arquivo se chama `index.html` (minúsculas, sem `.txt` escondido no final)? `Index.html` ou `renascer-sistema.html` **não** funcionam.
- Ele está na raiz do repositório, e não dentro de uma pasta como `github-pages/index.html`?
- Em *Settings › Pages*, a pasta escolhida é `/ (root)` e a branch é `main`? Se você escolheu `/docs`, o arquivo precisa estar em `docs/index.html`.
- O deploy terminou? Em **Actions** (aba do repositório) o último *pages build and deployment* deve estar verde. Use Ctrl+F5 para limpar o cache.
- O endereço está certo? Em site de projeto, é `usuario.github.io/NOME-DO-REPOSITÓRIO/`, e não `usuario.github.io/`.

## Como usar e o que esperar

- No primeiro acesso aparece **"Primeiro acesso"**: crie o administrador (nome, e-mail e senha). Depois cadastre os demais usuários em **Configurações**.
- **Os dados ficam salvos no navegador de quem usa** (cada computador/navegador tem a sua cópia). Não há banco compartilhado entre computadores.
  Se limpar os dados do navegador, as informações somem. Para ter um banco de dados de verdade, use o backend NestJS com Neon/Supabase (pasta `erp-distribuidora`).
- O login desta página **não é segurança de verdade** (roda no próprio navegador). Não use senhas que você usa em outros lugares.
- Sites do GitHub Pages são **públicos**: qualquer pessoa com o endereço abre a tela de entrada, e o código-fonte contém os dados cadastrais
  da empresa e da conta bancária de exemplo (CNPJ, endereço, banco, agência, conta e chave PIX). Isso não dá acesso aos seus dados salvos,
  mas se não quiser expor esses dados, peça uma versão sem eles.
