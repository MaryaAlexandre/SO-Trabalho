# Chamada UpTime 
É usada para obter informações sobre o tempo de atividade do sistema. Uptime retorna o tempo que o sistema foi inicializado até o momento atual, bem como como informações realizadas a carga média do sistema. Através da função "<sys/sysinfo.h>" é usada para obter informações sobre o sistema. Utilzando essa também para armazenar as informações sobre o sistema. Chamando a função Sysinfo(), passando um ponteiro para a estrutura "info" para armazenar as informações do sistema, se a chamada falhar uma mensagem de erro será impressa e o programa vai se encerrar. Com as informações através de "Sysinfo" executei um calculo para o tempo (horas, minutos e segundos), correspondente ao tempo de atividade e ao final mostrando a saída de uma maneira legível. 

Dessa forma será mostrado de maneira programática a chamada de sistema UpTime, chamada necessária para fornecer informações essenciais do sistema, monitoramento de desempenho, planejamento de manutenção, disponibilidade de recursos, detecção de picos de uso. 
## Foi utilizado Sysinfo - struct Sysinfo.


# Chamada Cat 
A chamada cat é utilizada para ler e escrever arquivos, é usada para concatenar e exibir conteúdo de arquivos de texto, por exemplo cat arquivo.txt exibirá o conteúdo do arquivo arquivo.txt no terminal. Utilizei as bibliotecas "fstream" para manipulação de arquivo e "string" para a manipulação de string, inicialmente verificando se o programa foi chamado com exartamente dois argumentos- o nome do programa e o nome do arquivo, após é atribuido o nome do arquivo que se deseja ler à variável do arquivo. Utilizei "std::ifstream" para abrir o arquivo especificado em modo de leitura e caso não seja possível será impressa uma mensagem e o programa termina com um código de erro, o conteúdo também será lido linha por linha onde cada linha é armazenada na variável linha e depois impressa na saída padrão. Utilizando essas funções desta maneira é possível realizar a chamada de sistema Cat porém de maneira programática.
## Foram utilizadas as bibliotecas <fstream> e <string>, funções "is.open", "getline","fstream".

 # Chamada Cp
A chamada cp é utilizada para copiar arquivos ou diretórios de um local para outro, para realizar essa chamada de maneira programática, eu utilizei  biblioteca "<fstream>" para conseguir ler e escrever esses arquivos, na primeira parte verificando se o programa foi chamado com três argumentos- o nome do próprio programa, o nome do arquivo de origem e o nome do arquivo de destino, exibindo uma mensagem de erro caso não passe com três argumentos. Utilizando também ponteiros como forma de receber a atribuição dos caracteres de origem  e destino. Para abrir o arquivo de origem, foi utilizado a forma de leitura binária, realizando-se assim a chamada de sistema porem de maneira programática.
## Foi utilizado a biblioteca <fstream>, funções "rdbuf" (para retornar o ponteiro/ direção da informação. 


# Chamada Ls
A chamada de sistema Ls é utilizada para ler e listar todos os arquivos dentro de um diretório, de maneira programática para se realizar a chamada foi se usado a função "opendir", para abrir o diretório especificado, sendo assim a lógica básica utilizada no código foi verificar se o diretório foi especificado como argumento, caso nenhum seja especificado será usado o diretório atual(o que estiver presente), vai ser definido uma variável contendo o que se deseja listar e para finalizar é utilizado a função readdir para ler os arquivos dentro do diretório que foi aberto.
## Utilizados Opendir e Readdir.

# Chamada Mkdir
A chamada de sistema Mkdir é utilizada para criar um novo diretório, de maneira programática para se criar uma chamada Mkdir é necessário verificar se o diretório já existe utilizando a função "createDirectory" através de bibliotecas <sys/stat.h> e <string>. E caso não exista será criado um novo diretório com "struct stat info", atravês de info.st_mode e S_IFDIR vai se verificar se o caminho já existe mas não é um diretório, realizando assim uma chamada de sistema porém de maneira programática.
## Foi utilizado "createDirectory", "struct", "stat", info.st_mode, S_IFDIR bem como as bibliotecas <sys/stat.h> e <string>.

# Chamada Rm-r Rdmir
É um comando usado em sistemas unix-like para remover arquivos e diretórios, -r é uma opção do comando rm que indica que a remoção é feita de maneira recursiva ou seja além de remover o diretório especificado, todos os rquivos e subidiretórios dentro dele também vão ser removidos. Para realizar a chamada de sistema através de um código de alto nível em c++, eu utilizei filesystem como suporte para operar arquivos, caminhos (diretórios) e assim poder manipula-los. Inicialmente utilizei um teste para verificar se o caminho existe e se há um diretório para ele, após vou atualizar quanto aos itens pertencentes ao diretório e caso o item seja um diretório sera chamado recursivamente "remove_directory" uma função para caso o item seja um arquivo ser removido. Também foi implementado a remoção do diretório vazio, mensagens em caso de erro de remoção de diretório, e a pavimentação ou seja a informação do diretório a ser removido.

Portanto o comando é usado para remover diretórios e seu conteúdo de forma recursiva, utilizando nesse caso filesystem para realizar a  chamada de sistema, mas de forma programática.
## Foi utilizado "remove", "exists", "is_directory" - funções, biblioteca <filesystem>.

# Chamada de sistema Chmod
A chamada de sistema Chmod é utilizada para alterar permissões de arquivos, de maneira programática a realização da chamada de Chmod é necessário se verificar e o caminho especificado pelo usuário existe na função, se o caminho existir continuamos com as alterações. É visto também as exceções que podem ser lançadas durante a execução das instruções.
Para isso se utilizou "Change_permissions" que recebe dois parâmetros o caminho do rquivo ou diretório, verifica se o caminho existe, usa "exists" para continuar com as alterações caso o caminho exista. Dessa maneira realizando as alteraçõe de permissão de maneira programática.
##Foi utilizado change_permissions, exists, chmod, c_str, expection, what, mode_t.

# Chamada de sistema Chown
A chamada de sistema Chown muda o dono do arquivo/ grupo ao qual ele pertence, de maneira programática a chamada de sistema Chown vai verificar se o caminho existe "exists", alterar o dono do arquivo "permissions", "remove", bem como solicitar ao usuário o caminho e diretório. Usando "change_owner" função para alterar o dono/ grupo. Realizando assim de maneira programática a realização da chamada de sistema de maneira programática.
## Foi utilizado biblioteca <Filesystem>, change_owner - função, "exists", permissions, exception.

# Chamada de sistema Mv
A chamada de sistema Mv é utilizada para mudar de lugar/nome um arquivo de maneira programática se as bibliotecas <cstring>, <cerrno>, <unistd.h>, é necessário atribuir os nomes dos arquivos de origem e destino aos ponteiros, vai mover o arquivo "rename" para mover o arquivo da origem para o destino, se não for possível uma mensagem de erro vai aparecer. 
## Foi utilizado "rename", "strerror", e de bibliotecas <Cstring>, <cerrno>, <unistd.h>.

# Chamada de sistema Rm
A chamada de sistema Rm é utilizada para remover arquivos, de maneira programática é necessário verificar se o programa foi chamado com exatamente dois argumentos - o nome do próprio programa e o nome do arquivo que se deseja remover. "unlink" será usado para remover o arquivo especificado, se a remoção do arquivo falhar uma mensagem de erro será impressa.
## Foi utilizado para isso "unlink", de biblioteca <unistd.h>.





