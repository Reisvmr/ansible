# ansible
Este projeto concentra laboratorios do curso de ansible, que conta com duas VMs VirtualBOx, centos 7.2 e debian 9, conectadas em rede (modo bridge saindo direto para internet)
Este documento vai agregar anotaçoes relevantes das aulas.


ambiente do curso:

hostAnsible: notecasa:192.168.0.13
guests:
	centos: 192.168.0.34 (centos 7.2)
	debian: 192.168.0.35 (debian 9  )

instalação: 
```apt install ansible```

####################################################################
informações do pacote: 
ansible 2.8.3
  config file = /etc/ansible/ansible.cfg
  configured module search path = ['/home/ramonrrp/.ansible/plugins/modules', '/usr/share/ansible/plugins/modules']
  ansible python module location = /usr/lib/python3/dist-packages/ansible
  executable location = /usr/bin/ansible
  python version = 3.7.5 (default, Nov 20 2019, 09:21:52) [GCC 9.2.1 20191008]
####################################################################

exemplos: ansible [ip, subdivisoes no hosts]
	-i - iventario	
	-m - modulo
	-a - argumentos
	-u - usuario
	-k - senha do usuario
	-K - SENHA DO SUDO
	-b - executar como super usuario
	-v - verbose

ansible all -i hosts -u root -k -m systemd -a  "name=sshd state=restarted"

##
4 - inventory
##

##
5 - são funções que executam tarefas
##
estrutura padrão das pastas:
   roles/
   └── common
       ├── defaults - variaveis globais
3.     ├── files
2.     ├── handlers - manipuladores de eventos acionados por task
6.     ├── meta - primeiro diretorio a ser visto
1.     ├── tasks - relação de tarefas a serem executadas 
4.     ├── templates
5.     └── vars - variaveis adicionais da role
*sempre deve haver um arquivo main.yml*

system facts: variaveis com informações dos sistemas descobertas pelo modulo setup

**files são arquivos estáticos. Templates são dinâmicos
