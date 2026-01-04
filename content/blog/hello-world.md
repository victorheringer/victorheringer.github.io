+++
title = "Olá, Mundo!"
date = "2025-09-04"
description = "Primeira postagem do meu blog, onde conto como criei esse site com Hugo, Docker e GitHub Pages."
tags = []
+++

Este é o primeiro post do blog e, para inaugurar, vou deixar registrado como tudo foi montado. A ideia foi manter o processo bem prático e fácil de repetir.

## Como o site nasceu

Eu usei o [Hugo](https://gohugo.io/), que é um gerador de site estático. Ele é rápido, tem uma estrutura organizada e funciona muito bem para esse tipo de projeto — principalmente quando você quer focar no conteúdo e não em um monte de infraestrutura.

Para não depender de instalação local (e para manter o ambiente consistente), eu rodei o Hugo via Docker, usando a imagem da comunidade: [`klakegg/hugo`](https://hub.docker.com/r/klakegg/hugo/). Assim, dá para criar o site, servir localmente e gerar o build final sem “poluir” o sistema com dependências.

O visual do blog vem do tema [hugo-bearblog](https://github.com/janraasch/hugo-bearblog). Eu gosto justamente porque ele não tenta ser mais do que precisa: é limpo, legível e deixa o texto em primeiro plano.

## Publicação no GitHub Pages

Para colocar no ar, escolhi o [GitHub Pages](https://pages.github.com/). O fluxo é bem tranquilo: eu gero o site com o Hugo e publico os arquivos estáticos no branch `gh-pages`, que é o que o GitHub usa para servir o conteúdo.

No fim das contas, a receita fica assim:

- **Hugo** gera o site;
- **Docker** deixa o ambiente simples e repetível;
- **Bearblog** dá um visual minimalista e confortável de ler;
- **GitHub Pages** hospeda tudo sem custo.

Se você tiver curiosidade, o repositório está aqui:

- https://github.com/victorheringer/victorheringer.github.io

## E agora?

A partir daqui, a ideia é usar este espaço para registrar aprendizados, projetos e coisas que eu for achando interessantes — tanto dentro quanto um pouco fora do mundo de desenvolvimento.

Se você curte desenvolvimento web/mobile, interfaces, eletrônica ou aquela nostalgia 8-bit, acho que você vai se sentir em casa.

Até a próxima!
