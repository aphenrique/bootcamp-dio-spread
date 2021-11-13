[Voltar para a página inicial](./README.md)
# Índice

[TOC]

# Objetos fundamentais do git

- Blob
    - Bloco básico de composição
    - Armazena o sha1
    - Contém metadados do git — Tipo do objeto, tamanho da string, nome do arquivo
    - Seria o equivalente ao arquivo
- Tree
    - Armazena um conjunto de blobs
    - Armazena o nome do arquivo
    - É responsável por montar a estrutura de onde estão os arquivos
    - Também possui um sha1 prórpio
- Commits
    - Objeto que agrupa e torna coeso o conjunto de informações guardados na árvore e nos blobs
    - Aponta para uma árvore
    - Aponta para o commit anterior
    - Aponta para um autor
    - Aponta para uma mensagem
    - Possui um timestamp

# Comandos básicos

- git init
    - inicia o repositório git local
- git add
    - adiciona os arquivos "untracked" (ainda não listados, desconhecidos do repositório) para a lista de staged
    - adiciona os arquivos que estavam "modified" para a lista de "staged" (preparados para commit)
- git commit -m "<mensagem>"
    - Consolida as alterações no repositório movendo os arquivos "staged" para "unmodified"
- git push <alias do repositório remoto>
    - Envia o repositório local para o repositório remoto com todos os commits e suas informações
- git pull
    - Puxa do repositório remoto as informações, arquivos e o for necessário para que o repositório local reflita o remoto

# Como resolver conflitos

- Quando existe um conflito de merge
    - Busca o repositório remoto (git pull)
    - Abre o arquivo, resolve o conflito (define como o arquivo deve ficar)
    - Adiciona à stage (git add <arquivo>)
    - Manda o repositório local para o remoto
