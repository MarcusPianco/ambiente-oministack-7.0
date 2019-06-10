# Ambiente OminiStack 7.0

Este repositório tem o propósito de ajudar na instalação de biblioteças e configurações necessárias para o desenvolvimento de aplicações na semana oministack 7.0 da rocketseat, este repositório não tem qualquer vínculo não sendo atrelado ao curso, foi apenas criado para ajudar alguns devs a instalar o que é preciso :).

# Configurando o nodeJS versão LTS

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

