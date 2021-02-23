# Slackckware (Stable)

Esse repositório inclui apenas os pacotes pré-compilado mais comuns para arquitetura x86_64 do Slackware (Stable).

Página inicial:      https://slackware.com/ <br/>
Suporte:             https://www.linuxquestions.org/questions/slackware-14/ <br/>
Relatório de erro:   https://www.linuxquestions.org/questions/slackware-14/ <br/>


Pacote de terceiros: https://slackbuilds.org


### O que são os Slackbuilds

São shell scripts com a função de automatizar a criação de pacotes tgz para o Slackware, e devem se encontrar no 
diretório source do programa a partir do qual será gerado o pacote tgz.


Esses pacotes compilados, podem ser instalados usando o comando installpkg.


Exemplo:

Obs: Dependendo do pacote pode possui uma série de dependências.

```javascript

which sbopkg
/usr/sbin/sbopkg


sbopkg -g wvdial
Searching for wvdial
Found the following matches for wvdial:
network/wvdial


sqg -p wvdial
Processing wvdial.
Done.

cat /var/lib/sbopkg/queues/wvdial.sqf 
wvstreams
wvdial


installpkg /tmp/wvstreams-4.6.1-x86_64-2_SBo.tgz
installpkg /tmp/wvdial-1.61-x86_64-2_SBo.tgz


ls -l /var/log/packages/ | grep -i wvdial
-rw-r--r-- 1 root root    1173 Fev  1 23:03 wvdial-1.61-x86_64-2_SBo


which wvdial
/usr/bin/wvdial

```

