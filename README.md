Entrar no diretório do FTP e rodar o comando 

cd docker-ftp && sudo docker build . -t pipoca:1.0

sudo docker images 

pegar o image-id do container e colocar no final do comando abaixo:


# Usage FTP
	$ docker run -d -v $PWD/../docs:/home/vsftpd \
					-p 20:20 -p 21:21 -p 47400-47470:47400-47470 \
					-e FTP_USER=<username> \
					-e FTP_PASS=<password> \
					-e PASV_ADDRESS=<ip address of your server> \
					--name ftp \
					--restart=always <imagem gerada pelo build>


Entrar no diretório do NGINX e rodar o comando


cd docker-nginx && docker build . -t popcorn:1.0

sudo docker images 

pegar o image-id do container e colocar no final do comando abaixo:


# Usage NGINX
        $ docker run -d -v $PWD/../docs:/var/www/html/ -p 80:80 -it <imagem gerada pelo build>
