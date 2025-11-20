---
title: GIT
# date: 2025-11-19
tags: [terminal, git, personal]
draft: false
---

<!--more-->

## Comandos básicos do Git

### `git init`
Inicia um novo repositório Git em um diretório.
```bash
git init
```

Cria um novo repositório enquanto especifica o nome do projeto.
```bash
git init [nome_do_projeto]
```

### `git add`
Prepara alterações em arquivos para o próximo commit:
```bash
git add nome_do_arquivo
```
Adiciona todos os arquivos de uma vez:
```bash
git add .
```
### `git commit`
Cria uma mensagem de commit para as alterações, tornando-as parte do histórico do seu projeto:
```bash
git commit -m "Adicionar novo recurso"
```
### `git status`
Exibe informações importantes sobre as modificações e o status de preparação de seus arquivos.
```bash
git status
```
### `git log`
Permite visualizar uma lista cronológica do histórico de commits:
```bash
git log
```
### `git diff`
Compara as alterações entre o diretório de trabalho e o commit mais recente. Por exemplo, **esse uso** do git diff identifica as diferenças em um arquivo específico:
```bash
git diff arquivo1.txt
```
Para comparar as alterações entre dois commits, use o seguinte:
```bash
git diff commit1 commit2
```
### `git rm`
Remove arquivos do seu diretório de trabalho e prepara a remoção para o próximo commit.
```bash
git rm arquivo1.txt
```
### `git mv`
Renomeia e move arquivos em seu diretório de trabalho. Aqui está o comando do Git para renomear um arquivo:
```bash
git mv arquivo1.txt arquivo2.txt
```
Para mover um arquivo para um diretório diferente, digite:
```bash
git mv arquivo1.txt nova_pasta/
```
### `git config`

Configura vários aspectos do Git, incluindo informações e preferências do usuário. Por exemplo, digite esse comando para definir seu endereço de e-mail para os commits:
```bash
git config --global user.email "seu-email@exemplo.com"
```
O sinalizador `-global` aplica as configurações universalmente, afetando seu repositório local.

## Comandos de branch e merge

### `git branchi`
gerencia ramificações em seu repositório Git. Aqui está o uso básico do git branch para listar todas as ramificações existentes:
```bash
git branch
```
Para criar um branch chamada “recurso”, use:
```bash
git branch recurso
```
Renomeia um branch:
```bash
git branch -m nome-do-branch novo-nome-do-branch
```

### `git checkouti`
Permite alternar entre ramificações e restaurar arquivos de diferentes commits.
Mudar para um branch existente:
```bash
git checkout nome_do_branch
```
Descarta alterações em um arquivo específico e revertê-lo para o último commit:
```bash
git checkout -- nome_do_arquivo
```
### `git merge``
Mescla um branch de recurso ou tópico no branch principal. Abaixo está um exemplo de uso do `git merge`:
```bash
git merge nome_do_branch
```
### `git cherry-pick`
Permite que aplicar commits específicos de um branch para outro sem mesclar um branch inteiro.
```bash
git cherry-pick commit_hash
```
### `git rebase`
Aplica alterações de um branch do Git em outro, movendo ou combinando commits. Ele ajuda a manter um histórico de commits mais limpo:
```bash
git rebase main
```
### git tag
Marca pontos específicos em seu histórico do Git, como v1.0 ou v2.0:
```bash
git tag v1.0
```
## Comandos de repositório remoto Git

### `git clone`
Cria uma cópia de um repositório remoto em seu computador local. Um exemplo de uso básico do `git clone` é clonar um repositório do GitHub:
```bash
git clone https://github.com/username/meu-projeto.git
```
### `git push`
Envia os commits do branch local do Git para um repositório remoto, atualizando-o com suas alterações mais recentes.
Se desejar enviar as das alterações do repositório local chamado “principal” para o repositório remoto chamado “origem”:
```bash
git push origem principal
```
### `git pull`
Obtém e integra as alterações de um repositório remoto em seu branch local atual. Aqui está um exemplo de uso do git pull para extrair alterações do branch principal:
```bash
git pull origem mestre
```
### `git fetch`
Recupera novos commits de um repositório remoto sem mesclá-los automaticamente em seu branch atual, use este comando:
```bash
git fetch origem
```
### `git remote``
Gerencia os repositórios remotos associados ao seu repositório local.
Lista os repositórios remotos configurados no projeto:
```bash
git remote
```
Lista os nomes e as URL associadas a cada diretório remoto:
```bash
git remote -v
```
Para adicionar um novo repositório remoto, especifique seu nome e URL: 
```bash
git remote add origem https://github.com/username/origem.git
```
### `git submodule`
Usado para gerenciar repositórios separados incorporados dentro de um repositório Git.
Para adicionar um submódulo ao seu repositório principal, use:
```bash
git submodule add https://github.com/username/submodule-repo.git caminho/do/submodulo
```
## Comandos avançados do Git

### `git reset`
Desfaz alterações e manipula o histórico de commits.
```bash
git reset arquivo1.txt
```
### `git stash`
Armazena alterações temporárias que ainda não estão prontas para receber o commit.
```bash
git stash
```
Para ver uma lista dos armazenamentos temporários:
```bash
git stash list
```
Para aplicar a alteração mais recente e removê-la da lista de alterações temporárias:
```bash
git stash pop
```
### `git bisect`
Usado principalmente para identificar bugs ou problemas no histórico do seu projeto.
Para iniciar o processo de bissecção:
```bash
git bisect start
```
Usando o comando abaixo, o Git navegará automaticamente pelos commits para encontrar os que apresentam problemas:
```bash
git bisect run <test-script>
```
### `git blame`
Determina o autor e a alteração mais recente em cada linha do arquivo:
```bash
git blame arquivo1.txt
```
### `git reflog`
Faz um registro das alterações de um branch do Git. Ele permite que você acompanhe a linha do tempo do seu repositório, mesmo quando os commits são excluídos ou perdidos:
```bash
git reflog
```
### `git clean`
Remove arquivos não rastreados de seu diretório de trabalho, o que resulta em um repositório mais limpo e organizado:
```bash
git clean [options]
```
As [options] podem ser personalizadas com base em suas necessidades específicas, como -n para uma execução seca (dry run), -f para forçar ou -d para diretórios.



## Mostar repositório remoto
- `git remote -v`: Mostra o repositório remoto.
- `git remote get-url origin`: Mostra apenas o URL do repositório remoto.
- `git remote get-url --push <nome-do-remoto>`: Se tiver mais de um remoto (ex.: upstrem, fork, etc.)
- `git remote show origin`: Mostra detalhes completos da configuração.
- `git config --get remote.origin.url`: Mostra só o push do origin do repositório remoto atual. 

## Referências:
[Comandos Git: uma lista dos mais usados para simplificar seu trabalho](https://www.hostinger.com/br/tutoriais/comandos-git?utm_campaign=Generic-Tutorials-DSA-t3%7CNT:Se%7CLO:BR&utm_medium=ppc&gad_source=1&gad_campaignid=19588998604&gbraid=0AAAAADMy-hbelzrSz2wqeXvzkYn-l-XdG&gclid=Cj0KCQiA5abIBhCaARIsAM3-zFUZ2nhGcfS3FwDh4lO8-EVh3HABQ3_3lhxkMlaAeAIDPr3fa4bUg6YaAiniEALw_wcB). Disponível em: \<https://www.hostinger.com/br/tutoriais/comandos-git?utm_campaign=Generic-Tutorials-DSA-t3%7CNT:Se%7CLO:BR&utm_medium=ppc&gad_source=1&gad_campaignid=19588998604&gbraid=0AAAAADMy-hbelzrSz2wqeXvzkYn-l-XdG&gclid=Cj0KCQiA5abIBhCaARIsAM3-zFUZ2nhGcfS3FwDh4lO8-EVh3HABQ3_3lhxkMlaAeAIDPr3fa4bUg6YaAiniEALw_wcB>. Acesso em: 04 nov. 2025.
