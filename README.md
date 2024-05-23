# Init Linux

## Atualizações iniciais

Atualiza a lista de pacotes disponíveis:

`sudo apt upgrade`

Instala as versões mais recentes dos pacotes instalados no sistema:

`sudo apt update`

## Instalar Programas

### Snap Store

-   VS Code
-   Postman
-   Spotify
-   Gpt-desktop

#### Node.js

1.  Baixar o prebuilt:
    -   https://nodejs.org/en/download/prebuilt-binaries
2.  Criar pasta localmente:
    -   `sudo mkdir -p /usr/local/lib/nodejs`
3.  Extrair arquivo e mover:
    -   `sudo tar -xJvf node-v20.13.1-linux-x64.tar.xz -C/usr/local/lib/nodejs`
4.  Abrir Profile:
    -   `nano ~/.profile`
5.  Adicionar:
    -   `#Nodejs`
    -   `export PATH=/usr/local/lib/nodejs/node-v20.13.1-linux-x64/bin:$PATH`
6.  Refresh profile:
    -   `~/.profile`

#### Git

1.  Instalar Git:
    -   `sudo apt install git`
2.  Verificar chave ssh:
    -   `ls ~/.ssh`
3.  Gera uma chave ssh:
    -   `ssh-keygen -t rsa -b 4096 -C "ronaldmateus785@gmail.com"`
4.  Adiciona ao agente para não inserir a senha toda vez:
    -   `eval "$(ssh-agent -s)"`
    -   `ssh-add ~/.ssh/id_rsa`
5.  Copiar chave:
    -   `cat ~/.ssh/id_rsa.pub`
6.  Inserir no github:
    -   settings -> ssh and GPG Keys
7.  Testar conexão:
    -   `ssh -T git@github.com`
8.  Configurar git:
    -   `git config --global user.name "Ronald Almeida `
    -   `git config --global user.email "ronaldmateus785@gmail.com"`
    -   `git config --global init.defaultBranch main`

### Google

1.  Baixar arquivo deb: [Link](https://www.google.com/intl/pt-BR/chrome/)
2.  Instalar deb:
    -   `sudo dpkg -i google-chrome-stable_current_amd64.deb`
3.  Se houver dependências não atendidas:
    -   `sudo apt-get install -f`

#### Putty

1.  Instalar Putty:
    -   `sudo apt install putty`

#### FileZilla

1.  Instalar FileZilla:
    -   `sudo apt install filezilla`

#### MongoDB Compass

1.  Baixar arquivo deb: [Link](https://www.mongodb.com/try/download/compass)
2.  Instalar deb:
    -   `sudo dpkg -i mongodb-compass_1.43.0_amd64.deb`
3.  Se houver dependências não atendidas:
    -   `sudo apt-get install -f`
