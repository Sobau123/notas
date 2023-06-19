# Inicializando git Local


Primeiro confira se o git está instalado:

```bash
$ git --version
```

Segundo, como colocar seu nome e seu email:

```
$ git config --global user.name "Seu Nome"
$ git config --global user.email "seuEmail@gmail.com"
```

Terceiro, criar o arquivo que deseja fazer com:

```
$ cd Documents/
$ mkdir arquivo (exemplo:notas)
```

Para ver o que tem dentro da pasta você usa:

```
$ls
```

Para ter a autorização de mexer no arquivo tem que usar:

```
$ git init
```

E para mexer no arquivo você usa entra no visual studio code com:

```
$ code .
```

# Comandos do Github

Verificar estado dos arquivos/diretórios

```
git status
```

Adicionar um arquivo em específico
````
git add meu_arquivo.txt
````

Adicionar todos os arquivos/diretórios
````
git add .
````

Comitar um arquivo
```
git commit meu_arquivo.txt
```

Comitar informando mensagem
```
git commit meuarquivo.txt -m "minha mensagem de commit"
```

Este comando deve ser utilizando enquanto o arquivo não foi adicionado na staged area.
```
git checkout -- meu_arquivo.txt
```

E para alteração do diretório pode ser utilizada o comando abaixo:
```
git checkout meu_arquivo.txt
```

Atualizar repositório local de acordo com o repositório remoto
--
Atualizar os arquivos no branch atual
```
git pull
```
Buscar as alterações, mas não aplica-las no branch atual
```
git fetch
```
Enviar arquivos/diretórios para o repositório remoto
--
O primeiro push de um repositório deve conter o nome do repositório remoto e o branch.
```
git push -u origin master
```
Os demais pushes não precisam dessa informação
```
git push
```
Branches
--
O master é o branch principal do GIT.

O HEAD é um ponteiro especial que indica qual é o branch atual. Por padrão, o HEAD aponta para o branch principal, o master.

Criando um novo branch
````
git branch bug-123
````
Trocando para um branch existente
````
git checkout bug-123
````
Neste caso, o ponteiro principal HEAD esta apontando para o branch chamado bug-123.

Criar um novo branch e trocar
````
git checkout -b bug-456
`````
Apagando um branch
````
git branch -d bug-123
````
Descartará quaisquer alterações locais não confirmadas nos arquivos correspondentes e, assim, restaurará seu último estado confirmado.
````
git restore
````
O arquivo será removido apenas da Staging Area - mas não alterará suas modificações.
````
git restore --staged bug-123
````