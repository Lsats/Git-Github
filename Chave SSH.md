Chave SSH: É uma forma de estabelecer uma conexão segura e encriptada entre duas máquinas.
Sempre há duas chaves, uma pública e uma privada.


Para gerar uma chave SSH para conectar seu Git ao Github:

Abra o GitBash e escreva:

#*ssh-keygen -t ed25519 -C “insira seu e-mail”*#

em seguida aparecerá um diretório para qual sua chave será enviada, caso deseje mudar certifique-se de digitar corretamente o novo diretório que não pode ser uma pasta (no meu exemplo utilizei um arquivo .txt)

*/h/Git/SSH*

após isso irá mostrar o diretório onde suas chaves foram colocadas, para redirecionar-se á elas faça:

*cd /H/Git*

use *ls* para listar e então aparecerá suas chaves privada e pública(.pub)

utilize o comando *‘cat’* para mostrar o conteúdo dentro da chave

*cat SSH.pub* 

você receberá a chave que deve colocar no seu GitHub

para ativar a mesma utilize os comandos:

*eval $(ssh-agent -s)*

e

*ssh-add SSH*


para ativar sua chave privada.
