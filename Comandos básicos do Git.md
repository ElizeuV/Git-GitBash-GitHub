# Comandos básicos do Git/Git Bash:coffee:

## Lista de comandos:

> limpa a tela:
```
clear ou ctrl + l 
```

> cria um diretório 
```
mkdir
```

> exibe, em formato largo, uma lista alfabética dos nomes de arquivo correspondentes em cada diretório
```
dir ou ls
```

> sai da pasta
```
cd .. 
```

> entrar na pasta
```
cd + nome da pasta 
```

> cria um novo repositório
```
git init 
```

> adiciona o arquivo ao diretório 
```
git add + nome do arquivo 
```

> adiciona todos arquivos (novos, modificados e removidos) ao diretório
```
git add .  
```

> clona o repositório remoto e cria uma cópia para o local do computador
```
git clone + link do repositório remoto 
```

> adiciona uma mensagem ao commit e faz o commit
```
git commit -m "mensagem" 
```

> exibe a lista de arquivos alterados
``` 
git status 
```

>envio/empurra o commit
```
git push  
```

> puxa/traz o commit
```
git pull  + link do dirtório
```

>  lista os commits feitos neste repositório em ordem cronológica inversa; isto é, o commit mais recente aparece primeiro
```
git log 
```

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

> Merge:
```
git merge desenvolvimento
```
```
git push origin main
```

### acessa o VsCode Web pelo GitHub
add file + ... 

### adiciona pessoas ao projeto (para comitar)
Settings > Collaborators > add people 

