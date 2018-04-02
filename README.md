# projetopassei
Projeto Passei Direto

Cada arquivo em anexo, corresponde a instalação e configuração dos seus proprios itens Localmente.

Pré-requisitos
Para seguir esse tutorial, você vai precisar do seguinte:

Droplet do Ubuntu 16.04 64 bits
Usuário não-root com privilégios sudo (Initial Setup Guide for Ubuntu 16.04 explica como configurar isto).

Nota: O Docker requer uma versão de 64 bits do Ubuntu, bem como uma versão de kernel maior ou igual a 3.10. O Droplet padrão de 64 bits do Ubuntu 16.04 atende a esses requisitos.

Todos os comandos nesse tutorial devem ser executados como usuário não-root. Se o acesso de root for requerido para o comando, ele será precedido pelo sudo. Initial Setup Guide for Ubuntu 16.04 explica como adicionar usuários e dar a eles o acesso ao sudo.

Passo 1 — Instalando o Docker
O pacote de instalação do Docker disponível no repositório oficial do Ubuntu 16.04 pode não ser a última versão. Para obter a maior e mais recente versão, instale o Docker a partir do repositório oficial do Docker. Essa seção lhe mostra como fazer isso.

Mas primeiro, vamos atualizar o banco de dados de pacotes:

sudo apt-get update
Agora, vamos instalar o Docker. Adicione ao sistema a chave GPG oficial do repositório do Docker:

sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D
Adicione o repositório do Docker às fontes do APT:

sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'
Atualize o banco de dados de pacotes com os pacotes do Docker a partir do novo repositório adicionado:

sudo apt-get update
Certifique-se de que você está instalando a partir do repositório do Docker em vez do repositório padrão do Ubuntu 16.04:

Finalmente, instale o Docker:

sudo apt-get install -y docker-engine
O Docker agora será instalado, o daemon iniciado, e o processo habilitado para iniciar no boot. Verifique que ele está executando:

sudo systemctl status docker
