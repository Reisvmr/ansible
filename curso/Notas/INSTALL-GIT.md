Todos os comando usados no vídeo: 

=========Instalação do .Git=========

 1º - Dependências do .Git

 - Comando:  apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \ libz-dev libssl-dev

 2º - Git

 - Comando: add-apt-repository ppa:git-core/ppa # apt update; apt install git
 ```
 apt-get install git
 ```
 -Clonar repository:

  ```
  git clone git@github.com:Reisvmr/ansible.git
   ```


================================

1º - Gerando a chave SSH do computador e colocando no Github
 - Comando: 
 ```
 ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
 ```
 - O arquivo gerado ficara localizado no diretoirio /home/SEUUSUARIO/.ssh/

================================
### CADASTRANDO CONTA NO VSCODE
================================
No terminal do vscode escrever as seguintes linhas:
```
git config --global user.email "reisvmr@gmail.com"
git config --global user.name "reisvmr"
git init
```