# Comandos Linux/Unix

São uma série de instruções que podem ser usadas para controlar um computador que executa um sistema operacional Linux ou Unix. Os comandos são geralmente escritos em uma linguagem de texto e são executados na linha de comando.

## Privilégios de usuário

- `sudo` (substitute user do) → Ele eleva os privilégios do seu usuário, por padrão ele eleva para superusuário. Também é usado para executar tarefas que exigem privilégios especiais, como instalar software, fazer alterações no sistema ou solucionar problemas.

## Navegação

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

## Manipulando arquivos e diretórios

- `cp` → Copia arquivos ou diretórios. **Exemplo:** `cp nome-do-arquivo`
    - `cp -r` (recursive)→ Copiará todos os arquivos e diretórios do diretório de origem para o diretório de destino, incluindo os subdiretórios e seus arquivos.
- `mv` → Move e ou renomeia arquivos e diretórios.
- `mkdir` (make directory) → Cria um novo diretório.
    - `mkdir -p` → cria um diretório, mesmo que os diretórios pai não existam.
- `rm` → Remove arquivos e diretórios.
    - `rm -f` → Remove arquivos sem solicitar confirmação.
    - `rm -r` → Remove diretórios recursivamente, incluindo os subdiretórios e seus arquivos.
- `touch` → É usado para criar um novo arquivo ou atualizar a data e hora de modificação de um arquivo existente.
**Dica:** Você pode usar o `nano` para criar e modificar arquivos também.

## Operadores úteis

- `;` → Usado para executar dois ou mais comandos em sequência. O primeiro comando é executado e, quando ele for concluído, o segundo comando será executado. Isso continua até que todos os comandos sejam executados.
**Exemplo:** `ls; pwd`
- `&&` → Parecido com o primeiro, porém, tem a diferença que o comandos seguinte só é executado apenas se o primeiro comando for bem-sucedido. O primeiro comando é executado e, se for bem-sucedido, o segundo comando será executado. Se o primeiro comando falhar, nenhum dos comandos será executado.
- `||` → Parecido com o anterior, porém, quando você executar dois ou mais comandos se o primeiro deles der erro ele ainda sim irá executar os comandos seguintes que estão corretos.
**Exemplo:**  `ls || pwd` o seguinte comando executará o comando `ls` e, em seguida, o comando `pwd` apenas se o comando `ls` falhar.
- `|` → Usado para redirecionar a saída de um comando para a entrada de outro comando. O primeiro comando é executado e sua saída é enviada para o segundo comando. O segundo comando recebe a saída do primeiro comando como entrada e a processa.
**Exemplo:** `ls | grep arquivo` esse comando executará o comando `ls` e enviará sua saída para o comando `grep`. O comando `grep` procurará a string "arquivo" na saída do comando `ls` e imprimirá as linhas que contêm a string "arquivo".
- `>` → Serve para redirecionar a saída de um comando para um arquivo. O comando é executado e sua saída é enviada para o arquivo especificado. O arquivo é criado se não existir, ou sobrescrito se já existir.
**Exemplo:** `ls > arquivo.txt` ****esse comando executará o comando `ls` e redirecionará sua saída para o arquivo `arquivo.txt`.
- `>>` → Server para anexar a saída de um comando a um arquivo. O comando é executado e sua saída é enviada para o arquivo especificado. O conteúdo do arquivo existente é mantido e a saída do comando é anexada ao final do arquivo.
**Exemplo:** `ls >> arquivo.txt` esse comando executará o comando `ls` e anexará sua saída ao arquivo `arquivo.txt`.
- `&` → Executa dois ou mais comandos em paralelo. Os comandos são executados simultaneamente e não precisam esperar um ao outro para terminar.
**Exemplo:** `ls & pwd` esse comando executará o comando `ls` e o comando `pwd` em paralelo.

## Backgroud e Foreground

- `jobs` → Usado para exibir uma lista dos trabalhos em andamento.
- `fg %n` → Traz o trabalho com o ID `n` para o primeiro plano. O comando `fg` sem nenhum argumento traz o primeiro trabalho em primeiro plano, enquanto o comando `fg` com um argumento traz o trabalho com o ID especificado para o primeiro plano.
**OBS:** O “n” serve somente como exemplo.
- `bg %n` → Coloca o trabalho com o ID `n` em segundo plano. O comando `bg` sem nenhum argumento coloca o último trabalho em segundo plano, enquanto o comando `bg` com um argumento coloca o trabalho com o ID especificado em segundo plano.
**OBS:** O “n” serve somente como exemplo.
- `kill %n` → Usado para matar um processo pelo seu nome ou id. O parâmetro `%n` é substituído pelo nome ou id do processo. Por exemplo, se você quiser matar o processo firefox, você usaria o seguinte comando: `kill %firefox`
**OBS:** O “n” serve somente como exemplo.

## Outros comandos

- `nano` → É um editor de textos, também pode ser usado para criar novos arquivos, editar arquivos existentes e salvar alterações em arquivos.
    - `Ctrl`+`O` → Salva as alterações no arquivo atual.
    - `Ctrl`+`X` → Sai do editor sem salvar as alterações.
    - `Ctrl`+`C` → Cancela a edição e sai do editor sem salvar as alterações.
    - `Ctrl`+`G` → Mostra o menu de ajuda.
- `file` → Descreve o tipo do arquivo.
- `history` → Mostra o histórico dos comandos digitados.
- `pkill` → Usado para matar processos com base em seu nome ou expressão regular. Ele é semelhante ao comando `kill`, mas o `pkill` permite que você mate processos com base em seu nome, em vez de seu ID de processo (PID).
- `whoami` → Mostra o usuário do sistema.
- `hostname` → Mostra o nome do computador.
- `uname` → Usado para imprimir informações sobre o sistema operacional. Ele imprime o nome do sistema operacional, o nome do host, a versão do kernel, a arquitetura do hardware e o tempo do sistema.
- `ps aux` → Lista todos os processos em execução, incluindo o nome do processo, o ID do processo (PID), o nome do usuário, o estado do processo, a CPU, a memória, a data e hora de início e o comando de inicialização.
