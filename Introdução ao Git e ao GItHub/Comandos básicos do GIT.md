# Comandos básicos do Git/Git Bash:coffee:

## Lista de comandos:

clear ou ctrl + l ➤ limpa a tela

mkdir ➤ cria um diretório 

dir  ➤ exibe, em formato largo, uma lista alfabética dos nomes de arquivo correspondentes em cada diretório

cd .. ➤  sai da pasta

cd + nome da pasta ➤ entrar na pasta

git init ➤ cria um novo repositório

git add + nome do arquivo ➤ adiciona o arquivo ao diretório 

git add .  ➤ adiciona todos arquivos (novos, modificados e removidos) ao diretório

git clone + link do repositório remoto ➤ clona o repositório remoto e cria uma cópia para o local do computador

git commit -m "mensagem" ➤ adiciona uma mensagem ao commit e faz o commit

git status ➤ exibe a lista de arquivos alterados 

git push ➤ envio/empurra o commit

git pull  ➤ puxa/traz o commit

git log ➤  lista os commits feitos neste repositório em ordem cronológica inversa; isto é, o commit mais recente aparece primeiro

> Mostra os comites em uma só linha:
```
git log --oneline 
```

> Volta para o commit anterior:
```
git restore --source + n° do hash do commit + . (todos arquivos)/(nome do arquivo)
```

> Se, em vez de menos informações, quisermos ver mais como as alterações do commit, podemos usar:
```
git log -p
```

> Também podemos pesquisar as informações do autor daquele commit com o comando:
```
git log --author="user_name"
```

>E pesquisar informações por data:
```
git log --since=1.month.ago --until=1.day.ago
```

>Você também pode formatar a visualização das informações de commit com o comando:
```
git log --pretty="format:%h %s"
```

>Vamos lá, como criar uma branch diferente? No terminal, vamos colocar o comando git checkout, -bpara criar a branch e chamarei essa branch de "desenvolvimento":
```
git checkout -b desenvolvimento
```

>Quando pressiono "Enter" ele cria a branch de desenvolvimento e estou nela agora. Se você quiser voltar para a branch principal pode usar o comando
```
git switch main. E para voltar para a branch de desenvolvimento: git switch desenvolvimento.
```

>Fiz um git add e um git commit, agora falta fazer um push para a nossa branch de desenvolvimento. Eu quero mandar para determinada origem, qual é essa origem? A origem de desenvolvimento:
```
git push origin desenvolvimento
```

>Merge
```
git merge desenvolvimento
```
```
git push origin main
```

> Anotações
```
[desenvolvimento bde3e52] Adicionando contato, branch desenvolvimento
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git brach
git: 'brach' is not a git command. See 'git --help'.

The most similar command is
        branch
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git branch
* desenvolvimento
  desenvolvimeto
  main
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro>  git branch -d  desenvolvimeto 
Deleted branch desenvolvimeto (was 21e7692).
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git branch
* desenvolvimento
  main
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git switch main                
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git branch
  desenvolvimento
* main
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git log --oneline
21e7692 (HEAD -> main, origin/main, origin/HEAD) Criação da página contato
fce427d voltando para: atualizando o arquivo app.js
43d25fd Atualizando a mensagem do arquivo console.log
a2d4e39 Atializando o a mensagem do arquivo console.log
c78559a atualizando o arquivo app.js
4ae0c56 .\app.js
e546ffd linkando o app js com o html
33d9cbe altereando o readme
4556665 criando o arquivo index do projeto
429fd4b alterando o readme do projeto
01a30cb criando arquivo js com o console
684f103 criando arquivo readme
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git merge desenvolvimento 
Updating 21e7692..bde3e52
Fast-forward
 contato.html | 3 +++
 1 file changed, 3 insertions(+)
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git log --oneline
bde3e52 (HEAD -> main, origin/desenvolvimento, desenvolvimento) Adicionando contato, branch desenvolvimento
21e7692 (origin/main, origin/HEAD) Criação da página contato
fce427d voltando para: atualizando o arquivo app.js
43d25fd Atualizando a mensagem do arquivo console.log
a2d4e39 Atializando o a mensagem do arquivo console.log
c78559a atualizando o arquivo app.js
4ae0c56 .\app.js
e546ffd linkando o app js com o html
33d9cbe altereando o readme
4556665 criando o arquivo index do projeto
429fd4b alterando o readme do projeto
01a30cb criando arquivo js com o console
684f103 criando arquivo readme
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> git push origin main           
Total 0 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ElizeuV/sistemas-de-cadastro.git
   21e7692..bde3e52  main -> main
PS C:\Users\Elizeu Vito Santos\Documentos\sistemas-de-cadastro> 
```

add file + ... ➤  acessa o VsCode Web pelo GitHub

Settings > Collaborators > add people ➤ adiciona pessoas ao projeto (para comitar)

