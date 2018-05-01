

i386 - retrocompatibilidade com arquiteturas antigas.
Dos - Windows - Ethernet.

Transporte - troca de contexto do kernel para SO - desenvolvimento de sockets pela aplicação.

InfiniBand - comunicação direta entre computadores - fazendo bypass do sistema operacional, diretamente no sistema de armazenamento do espaço de usuário da outra máquina.
Isso permite que o SO e CPU fiquem livres para outras operações enquanto a transferência é feita.

CPU é utilizada para registro de memória - a comunicação é poupada, mas CPU pode ser usada de outra forma.
protocolo baseada em hardware e bypass são as palavras-chave.

top500.org

Gibabit ethernet é alternativa no top500, mas a maioria é IB.

IB utiliza lanes, que permite paralelizar a transmissão de dados (via aplicação) para atingir o máximo de performance da IB.
QoS implementado por lane.

RDMA read and write - o problema é a sincronização, não tem como saber quando uma operação remota terminou, apenas implementando uma solução, como por exemplo interruptores para avisar quando uma operação terminou.

Utilizar total capacidade de IB:
verbis api - udapl - utilizar nativamente 

compatibilidade - virtualizar o adaptador infininand para ele aparecer como ethernet (com IP) e depois executar a aplicação normalmente.
OU
infinisocket e recompilar a aplicação para utilizar a infiniband.


SISTEMA TELEFONICO

AMPS
handoff - troca de celula por um dispositivo móvel - amps - 300 milis. 
pode acontecer que esteja online (falando ao telefone) - o usuário nem nota nesses 300 ms que trocou.
uma base entende 7 frequencias, cada celula base tem até 832 pessoas.

DAMPS - o próprio dispositivo detecta se o sinal está perdendo (MAHO), graças ao tempo ocioso adquirido por causa da multiplexação implementada. Então o dispositivo determina qual a estação base mais adequada, no caso de troca ele avisa a base que irá trocar e faz o handoff, também demorando 300 ms.
2/3 do tempo não está enviando nem recebendo sinal.

multiplexação no nível 1 - FDM - 
TDM - (tempo) até 6 usuários.  

