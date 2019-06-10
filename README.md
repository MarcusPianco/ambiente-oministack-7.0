# Ambiente OminiStack 7.0

Este repositório tem o propósito de ajudar na instalação de biblioteças e configurações necessárias para o desenvolvimento de aplicações na semana oministack 7.0 da rocketseat, este repositório não tem qualquer vínculo não sendo atrelado ao curso, foi apenas criado para ajudar alguns devs a instalar o que é preciso :).

# Instalndo o nodeJS versão LTS usando package manager

## macOs

1) Acesse o endereço:

https://nodejs.org/en/download/package-manager/
 
2) Escolha a opção macOs

 Existem duas opções:
 ### Via Bash inserindo o comando abaixo no terminal:
 
 ``
 curl "https://nodejs.org/dist/latest/node-${VERSION:-$(wget -qO- https://nodejs.org/dist/latest/ | sed -nE 's|.*>node-(.*)\.pkg</a>.*|\1|p')}.pkg" > "$HOME/Downloads/node-latest.pkg" && sudo installer -store -pkg "$HOME/Downloads/node-latest.pkg" -target "/"
 ``
 
### Ou usando HomeBrew

- Instale o HomeBrew

Abra o terminal e execute o seguinte comando:
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
``` 

Teste se o homebrew foi instalado corretamente digitando no terminal o comando: 
```
brew -v 
```
Deverá aparecer uma mensagem similar a esta:

```
Homebrew 2.1.1
Homebrew/homebrew-core (git revision 58f4; last commit 2019-04-21)
Homebrew/homebrew-cask (git revision 6586c; last commit 2019-04-20)
``` 


3) Instalando o Node com o HomeBrew
Basta digitar o comando: 
```
brew install node
```

Pronto, o Node já estará instalado no mac :)

## Linux

1) Basta Executar os seguintes comandos no terminal:

**Node.js v10.x**:

```sh
# Usando Ubuntu
curl -sL https://deb.nodesource.com/setup_10.x | sudo -E bash -
sudo apt-get install -y nodejs

# Usando Debian, como root
curl -sL https://deb.nodesource.com/setup_10.x | bash -
apt-get install -y nodejs
```

Pronto o node já está instalado!!!! :). Para testar execute noterminal o seguinte comando:

```sh
node -v
```
deverá aparecer a seguinte linha logo abaixo do comando:
`
v10.16.0
`

## Windows

###  Instalando o Chocolatey

1) Abra o powershell ou o cmd (como administrador)

2) Insira o seguinte comando no cmd ou powershell,como administrador:
```sh
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

Após instalar o  Chocolatey execute o seguinte comando no cmd ou powershell, como administrador.

```sh
cinst nodejs.install
```

O comando acima deverá instalar tanto o nodeJS quanto o npm(node package manager)

Pronto o nodeJS já está instalado :)!!!!

# Instalando o Yarn 

## macOS

Execute o seguinte comando no terminal(o homebrew deve estar instalado)
```sh
brew install yarn --without-node
```
Para testar se tudo deu certo execute o comando `yarn -v` e deverá aparecer: `1.15.2` ou algo similar 
## Linux

Execute o seguinte comando no terminal:
```sh
curl -o- -L https://yarnpkg.com/install.sh | bash
```
Para testar se tudo deu certo execute o comando `yarn -v` e deverá aparecer: `1.15.2` ou algo similar 

## Windos

Basta inserir o seguinte comando no cmd ou powershell, como administrador(o Chocolatey deve estar instalado)
```sh
choco install yarn
```
Para testar se tudo deu certo execute o comando `yarn -v` e deverá aparecer: `1.15.2` ou algo similar 

# Instalando o VS Code

1) Clique em aqui [Download VS Code](https://code.visualstudio.com/Download)

2) Escolha seu sistema operacional e é só fazer o download. :) !!!

# Instalando as Dependências no Vs Code

1) Clique em Extensions no VS Code 
![](/images/clicarextensionvscode.png)

## Instalando Tema Dracula

2) No campo busca digite `dracula` e clique em install como na imagem abbaixo:
![](/images/Instalandotemadracula.png)

Pronto o tema já está instalado :) !!! Caso o tema do seu vs code ainda não tenha mudado, clique nas opções seguintes (no meu superior do vs code)

```
Code->Preferences->Color Theme-> Dracula
```
A escolha da opção do tema pode variar de acordo com o seu sistema opracional, mas o processo será o mesmo( tenta localizar preferencias e logo em seguida tema :) )

## Modificando estilo dos Ícones 

1) novamente no campo de pesquisa em `extensions` ou `extensões` digite: `material` e busque a extensão 
`
Material Icon Theme
`
2) Clique em install 
Como na imagem abaixo:
![](/images/installicontheme.png)

Pronto o estilo de ícones já está instalado :) !!! Caso o tema do seu vs code ainda não tenha mudado, clique nas opções seguintes (no meu superior do vs code)

```
Code->Preferences->File Icon Theme->Material
```
A escolha da opção de mudança do estilo dos ícones pode variar de acordo com o seu sistema opracional, mas o processo será o mesmo( tenta localizar preferencias e logo em seguida File Icon Theme :) )



## Instalando Extensões da Rocketseat

1) novamente no campo de pesquisa em `extensions` ou `extensões` digite: `rocketseat`, aparecerão duas extensões, bas clicar em install como nas imagens abaixo:

2) Extensão Rocketseat ReactJS 
![](/images/extensionrocketseat.png)

3) Rocketseat React Native
![](/images/extensionrocketseat2.png)

Pronto as extensões da rocket seat já estão instaladas :) !!!

## Instalando FiraCode no VS Code

### macOS e Linux

1) Bas baixar o Fira Code no link: [FiraCode](https://github.com/tonsky/FiraCode/releases/download/1.206/FiraCode_1.206.zip)

2) Descompactar ir na pasta `/ttf/` clicar nas fontes e clicar em `Instalar Fonte` (no macos, no linux deverá ser similar),
faça isso para todos os arquivos .ttf na pasta.

3) Pressione as teclas command+shift+p no macOS  (no linux ctrl+shift+p) e digite `settings` clique na opção `Open Settings (JSON)`
e adicione as seguintes linhas dentro do arquivo settings.json:
```sh
"editor.fontFamily": "Fira Code",
"editor.fontLigatures": true
```
### Windows

Basta seguir esse post muito explicativo sobre como instalar o fira code font no windows:

https://imasters.com.br/desenvolvimento/fira-code-no-vscode

## Bônus

Para configurar o terminal para o tema dracula, use o tutorial da Rocketseat no blog oficial:

https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/


Obrigado Galera da Rocketseat !!!!:) 




