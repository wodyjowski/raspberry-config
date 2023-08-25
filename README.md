# raspberry-config

Raspberry Pi Zero uses ARMv6 instruction set so it needs a special NodeJS version: https://unofficial-builds.nodejs.org/download/release/v18.9.1/node-v18.9.1-linux-armv6l.tar.xz (https://unofficial-builds.nodejs.org)

Install NodeJs:
```
wget https://unofficial-builds.nodejs.org/download/release/v18.9.1/node-v18.9.1-linux-armv6l.tar.xz &&  
sudo mkdir -p /usr/local/nodeJS/bin &&  
sudo tar xvfJ node-v18.9.1-linux-armv6l.tar.xz -C /usr/local/nodeJS --strip-components=1 &&  
printf "\n#nodeJS\nPATH=$PATH:/usr/local/nodeJS/bin\n" >> ~/.profile
```

Uopdate package indexes:
```
DEBIAN_FRONTEND=noninteractive sudo apt-get -y git-all
```

Debian comes with preinstalled Apache server, to remove it use:
```
sudo apt purge apache2 apache2-utils
```
