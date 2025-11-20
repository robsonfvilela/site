---
title: Hugo
date: 2024-06-20
tags: [hugo, terminal]
---

Documentação de referência para gerenciar este blog.

<!--more-->

## Terminal

1. Criar um novo projeto:

    `hugo new site mysite`

2. Criar um novo post:
    
    `hugo new content/my-first-post.md`

3. Modelo de Post:

    ```yml
    ---
    title: "My First Post"
    date: 2024-06-20T12:00:00Z
    draft: true
    tags: [tag1, tag2]
    ---

    ## Introdução

    <!--more-->
    
    Seu conteúdo aqui.
    ```


2. Carregar o servidor local:

    `hugo server -t terminal --disableFastRender --noHTTPCache`
    - `-t`: define o tema a ser usado.
    - `terminal`: nome do tema`
    - `--disableFastRender`: desativa o renderização rápida para garantir que todas as mudanças sejam refletidas corretamente.
    - `--noHTTPCache`: desativa o cache HTTP para refletir as mudanças imediatamente.
