## Chamada UpTime 
É usada para obter informações sobre o tempo de atividade do sistema. Uptime retorna o tempo que o sistema foi inicializado até o momento
atual, bem como como informações realizadas a carga média do sistema. Através da função "<sys/sysinfo.h>" é usada para obter 
informações sobre o sistema. Utilzando essa também para armazenar as informações sobre o sistema. Chamando a função Sysinfo(), passando
um ponteiro para a estrutura "info" para armazenar as informações do sistema, se a chamada falhar uma mensagem de erro será impressa
e o programa vai se encerrar. Com as informações através de "Sysinfo" executei um calculo para o tempo (horas, minutos e segundos), correspondente
ao tempo de atividade e ao final mostrando a saída de uma maneira legível. 

Dessa forma será mostrado de maneira programática a chamada de sistema UpTime, chamada necessária para fornecer informações essenciais
do sistema, monitoramento de desempenho, planejamento de manutenção, disponibilidade de recursos, detecção de picos de uso. 

## Chamada Cat 
A chamada cat é utilizada para ler e escrever arquivos, é usada para concatenar e exibir conteúdo de arquivos de texto, por exemplo cat arquivo.txt
exibirá o conteúdo do arquivo arquivo.txt no terminal. Utilizei as bibliotecas "fstream" para manipulação de arquivo e "string"
para a manipulação de string, inicialmente verificando se o programa foi chamado com exartamente dois argumentos- o nome do programa e o nome 
do arquivo, após é atribuido o nome do arquivo que se deseja ler à variável do arquivo. Utilizei "std::ifstream" para abrir o arquivo
especificado em modo de leitura e caso não seja possível será impressa uma mensagem e o programa termina com um código de erro, o conteúdo também
será lido linha por linha onde cada linha é armazenada na variável linha e depois impressa na saída padrão. 
Utilizando essas funções desta maneira é possível realizar a chamada de sistema Cat porém de maneira programática.

Chamada Cp
A chamada cp é utilizada para copiar arquivos ou diretórios de um local para outro, 






Chamada Rm-r Rdmir
É um comando usado em sistemas unix-like para remover arquivos e diretórios, -r é uma opção do comando rm que indica que a remoção é
feita de maneira recursiva ou seja além de remover o diretório especificado, todos os rquivos e subidiretórios dentro dele também
vão ser removidos. Para realizar a chamada de sistema através de um código de alto nível em c++, eu utilizei filesystem como suporte 
para operar arquivos, caminhos (diretórios) e assim poder manipula-los. Inicialmente utilizei um teste para verificar se o caminho
existe e se há um diretório para ele, após vou atualizar quanto aos itens pertencentes ao diretório e caso o item seja um diretório
sera chamado recursivamente "remove_directory" uma função para caso o item seja um arquivo ser removido. Também foi implementado a remoção
do diretório vazio, mensagens em caso de erro de remoção de diretório, e a pavimentação ou seja a informação do diretório a ser removido.

Portanto o comando é usado para remover diretórios e seu conteúdo de forma recursiva, utilizando nesse caso filesystem para realizar a 
chamada de sistema, mas de forma programática.
