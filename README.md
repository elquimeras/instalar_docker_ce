# Instalar Docker-ce en Linux 
Instrucciones de instalación docker CE en Linux
Probado en Linux 16.04 && 18.04

1. Actulizar el apt / Update the apt package index:
	
	`sudo apt-get update`

2. Instale paquetes para permitir que apt use un repositorio sobre HTTPS / Install packages to allow apt to use a repository over HTTPS

	`sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common`

3. Agregar Clave GPG oficial de Docker: / Add Docker’s official GPG key

	`curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -`

4. Setear el repo / Set the repository

	`sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"`

5. Instalar Docker CE / Install Docker CE
	
	`sudo apt-get update`
	`sudo apt-get install docker-ce -y`

6. Agregar el usuario docker a lista de suoers / Add sudoer user for docker
	
	`sudo groupadd docker`
	`sudo gpasswd -a $USER docker`
	`sudo usermod -aG docker $USER`

7. Reinicia el terminal y prueba / Restart terminal and test

	`docker ps`

	- Si ves / If see

	`CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                    NAMES`

	- Docker fué instalado / Docker was installed
