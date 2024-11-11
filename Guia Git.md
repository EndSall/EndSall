# Comandos Essenciais e Avançados do Git

## Configuração Inicial
`git config --global user.name "Seu Nome"`  
Define o nome do usuário para todos os repositórios.

`git config --global user.email "seuemail@exemplo.com"`  
Define o e-mail do usuário para todos os repositórios.

`git config --global core.editor "nome-do-editor"`  
Define o editor de texto padrão para o Git (ex.: `vim`, `code`, etc.).

`git config --list`  
Lista todas as configurações atuais do Git.

## Iniciar no GitHub
Para conectar o repositório local ao GitHub, primeiro crie um repositório no site do [GitHub](https://github.com/).

### Conectar ao Repositório Remoto (GitHub)
`git remote add origin URL-do-repo-no-GitHub`  
Conecte o repositório local ao remoto no GitHub, substituindo pela URL do seu repositório.

`git remote -v`  
Verifica se a conexão foi estabelecida.

`git push -u origin main`  
Envia as alterações para o GitHub (na branch principal, geralmente `main` ou `master`).

`git clone URL-do-repo-no-GitHub`  
Caso você esteja começando com um repositório remoto existente no GitHub, use este comando.

### Operações Comuns com o GitHub
`git pull`  
Atualiza o repositório local com as mudanças do remoto, integrando alterações feitas por outros colaboradores.

`git push`  
Envia alterações locais para o GitHub depois de fazer `add` e `commit`.

`git checkout -b nome-da-branch` e `git push -u origin nome-da-branch`  
Cria e envia uma nova branch para o GitHub.

`git push origin --delete nome-da-branch`  
Exclui uma branch diretamente no GitHub.

## Criação e Inicialização de Repositório
`git init`  
Inicializa um novo repositório Git no diretório atual.

`git clone URL-do-repositório`  
Clona um repositório remoto para a máquina local.

## Manipulação de Arquivos
`git add .`  
Adiciona todas as alterações no diretório atual à área de staging.

`git add nome-do-arquivo`  
Adiciona um arquivo específico à área de staging.

`git rm nome-do-arquivo`  
Remove um arquivo do diretório e da área de staging.

`git mv arquivo_antigo arquivo_novo`  
Renomeia ou move um arquivo e atualiza o Git.

## Salvando Mudanças (Commits)
`git commit -m "Mensagem do commit"`  
Salva as mudanças na história do repositório com uma mensagem descritiva.

`git commit --amend -m "Nova mensagem"`  
Edita o último commit, alterando ou adicionando arquivos.

## Histórico
`git log`  
Exibe o histórico de commits no repositório.

`git log --oneline`  
Exibe o histórico de commits de forma resumida (uma linha por commit).

`git log --graph --decorate --oneline`  
Mostra o histórico de commits com um gráfico das branches.

`git blame nome-do-arquivo`  
Exibe cada linha de um arquivo com informações sobre o commit que a alterou.

## Branches (Ramificações)
`git branch`  
Lista todas as branches no repositório.

`git branch nome-da-branch`  
Cria uma nova branch.

`git branch -d nome-da-branch`  
Deleta uma branch local (só se ela já tiver sido mesclada).

`git checkout nome-da-branch`  
Troca para outra branch.

`git checkout -b nome-da-branch`  
Cria uma nova branch e troca para ela.

`git merge nome-da-branch`  
Mescla uma branch na branch atual.

`git rebase nome-da-branch`  
Realiza o rebase de uma branch na branch atual.

## Envio e Recebimento de Alterações
`git push`  
Envia os commits locais para o repositório remoto.

`git push -u origin nome-da-branch`  
Envia uma branch para o remoto e define como padrão.

`git push --tags`  
Envia todas as tags locais para o repositório remoto.

`git pull`  
Atualiza o repositório local com as alterações do remoto.

`git fetch`  
Baixa as mudanças do repositório remoto, sem mesclá-las.

## Reverter Alterações
`git checkout -- nome-do-arquivo`  
Desfaz mudanças em um arquivo não comitado.

`git reset nome-do-arquivo`  
Remove um arquivo da área de staging.

`git reset --soft HEAD~1`  
Remove o último commit, mantendo as mudanças na área de staging.

`git reset --hard HEAD`  
Reverte todas as mudanças locais para o último commit.

`git revert HASH-do-commit`  
Cria um novo commit que desfaz um commit específico.

## Tags
`git tag nome-da-tag`  
Cria uma tag no último commit.

`git tag -a nome-da-tag -m "Mensagem da tag"`  
Cria uma tag anotada com mensagem.

`git push origin nome-da-tag`  
Envia uma tag para o repositório remoto.

## Outras Opções Úteis
`git status`  
Exibe o status do repositório, como mudanças e arquivos em staging.

`git diff`  
Mostra diferenças entre o diretório de trabalho e o último commit.

`git diff nome-da-branch`  
Compara a branch atual com outra branch.

`git stash`  
Armazena temporariamente mudanças não comitadas.

`git stash pop`  
Restaura as mudanças salvas pelo último `git stash`.

`git cherry-pick HASH-do-commit`  
Aplica um commit específico de outra branch na branch atual.

`git bisect start`  
Inicia uma busca binária para localizar um commit que introduziu um bug.

## Aliases (Atalhos)
`git config --global alias.st status`  
Cria um alias `st` para o comando `status`.

`git config --global alias.co checkout`  
Cria um alias `co` para o comando `checkout`.

`git config --global alias.ci commit`  
Cria um alias `ci` para o comando `commit`.

`git config --global alias.br branch`  
Cria um alias `br` para o comando `branch`.