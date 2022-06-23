SHA1 - Arquivo de encriptação
Vai pegar um arquivo/foto etc e 'embaralhar' de forma específica, encriptar.

Objetos internos do Git:
- Blobs
- Trees
- Commits


Os arquivos ficam gravados dentro de objetos chamados *blob* no Git.
Geram sha1 (código de encriptação de 40 caracteres) diferentes do openssl sha1;

Estrutura básica do blob:
- Contém metadados dentro dele
- tipo do objeto - blob
- tamanho da string/arquivo
- \0 - barra contrária ao zero ou zero
- e o seu conteúdo







As *trees* armazenam blobs.
Trees, blobs e commits são uma crescente sendo o blob o bloco básico da composição.
- A tree sempre vai estar armazenando e apontando para tipos de blobs diferentes.
- A tree também possui o \0
- Uma tree aponta para um blob que por sua vez tem um sha1 e a tree guarda o nome do arquivo.
- A tree é responsável por montar toda a estrutura de onde estão localizados os arquivos.
- Elas podem apontar tanto para blobs quanto para outras trees
- As trees também são encriptadas
- Tem seu próprio sha1
- Caso mude algo no conteúdo dentro das trees/blobs o sha1 da blob e da tree irão mudar









Commit é o objeto que vai juntar tudo, que vai dar sentido ao que está sendo feito.
- O commit aponta para uma árvore (tree).
- Aponta para um parente (último commit realizado antes dele).
- Aponta para um autor e para uma mensagem.
- Commits também possuem sha1.



