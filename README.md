# Comandos Linux/Unix

São uma série de instruções que podem ser usadas para controlar um computador que executa um sistema operacional Linux ou Unix. Os comandos são geralmente escritos em uma linguagem de texto e são executados na linha de comando.

# Privilégios de usuário

- `sudo` (substitute user do) → Ele eleva os privilágios do seu usuário, por padrão ele eleva para superusuário. Também é usado para executar tarefas que exigem privilégios especiais, como instalar software, fazer alterações no sistema ou solucionar problemas.

# Navegação

**Dica:** o `-- help` serve para você ter uma ajuda de como utilizar o comando e quais a funcionalidades dele.

- `pwd` (print working directory) → Mostra a pasta ou diretório que você está atualmente
- `ls` (list) → Mostra (lista) tudo que tem no diratório atual
    - `ls -a` (all) → Lista todos os arquivos no diretório, incluindo os arquivos ocultos.
    **OBS:** Os arquivos ocultos são arquivos cujos nomes começam com um ponto (.). Por padrão, o comando ls não lista os arquivos ocultos.
    - `ls -l` (long) → Lista os arquivos em formato longo, que inclui informações como o tamanho, a data de modificação e os permissões do arquivo.
    - `ls -h` (human-readable) → Quando você usa a opção -h no comando ls, ele exibe os tamanhos dos arquivos em unidades legíveis por humanos, como KB, MB ou GB
    - **OBS:** Eu posso combinar todos os comando se eu quiser. **Exemplo:** `ls -a -l -h` ou eu posso fazer assim também `ls -la`
- `cd` (change directory) → É usado para mudar o diretório atual.
    
    **OBS:** Você irá digitar o comando e o caminho que você quer ir. Exemplo: `cd C:/Users/bruno/Contacts`
    
    - `cd .` → Representa o diretório atual
    - `cd ..` → Irá voltar uma pasta. Ele representa o diretório pai do diretório atual. Portanto, esse comando mudará para o diretório pai do diretório atual.
    **OBS:** Se eu quiser voltar varias patas o quanto que quiser é so fazer isso `cd ../../../` a cada dois pontos eu irei voltar uma pasta.
    - `cd -` → Faz você voltar para o direitório anterior que você estava. **Exemplo:** Se você estiver no diretório `/home/user` e usar o comando `cd /tmp`, o diretório atual será alterado para `/tmp`. Se você então usar o comando `cd -`, o diretório atual será alterado de volta para `/home/user`.
    - `cd ~`→ Faz você ir para a pasta home.
- `tree` → Serve para mostrar a árvore de todo o diretório que você. Dica: Caso não venha no seu OS você pode instalar o tree utilizando o comando no mac `brew install tree` e no linux `sudo apt isntall tree`
    - `tree -d` → Serve para mostrar só os diretórios.
    - `tree -a` → Serve para mostrar só os diretórios.
- `cat` → É usado para listar o conteúdo de arquivos e diretórios, ou seja, você consegue ler o conteúdo do arquivo. Ele também pode ser usado para combinar o conteúdo de vários arquivos em um único arquivo.
    - `cat -n` → Mostra o tanto de linhas que tem o arquivo.
- `tail` → Mostra as últimas linhas de um arquivo.
    - `tail -f` → Serve para ficar lendo o arquivo, atualizando em tempo real
- `wc` → É usado para contar o número de linhas, palavras e caracteres em um arquivo.
    - `wc -l` → Linhas.
    - `wc -m` → Caracteres.
    - `wc -w` → Palavras.
