# docker-help
Заметки по использованию docker 18.06.1-ce на Ubuntu 18.04.1 LTS (bionic)
## Установка Docker Community Edition на Ubuntu 18.04 LTS (bionic)
	```
	sudo apt-get update
	```
	
	```
	sudo apt-get install \
    	apt-transport-https \
    	ca-certificates \
    	curl \
    	software-properties-common
	```
	
	```
	curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
	```
	
	```
	sudo add-apt-repository \
   	"deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   	$(lsb_release -cs) \
   	stable"
	```
	
	```
	sudo apt-get update
	```
	
	```
	sudo apt-get install docker-ce
	```
Docker установлен.
	
# Команды
## Список активных и неактивных контейнеров:
	```
	$ sudo docker container ls -a
	```
## Запуск имеджа:
	```
	$ sudo docker run IMAGE_NAME
	```
## Билдинг имеджа с использованием тега, по которому позже его можно будет запускать. Имедж сбилдится только в том случае, если в директории есть Dockerfile:
	```
	$ sudo docker build -t YOUR_TAG_NAME .
	```
## Запуск имеджа с пробросом портов на хостовую машину:
	```
	$ sudo docker run -p 4000:80 IMAGE_NAME
	```
## Запуск в Detached-mode:
	```
	$ sudo docker run -d -p 4000:80 IMAGE_NAME
	```
## Остановка контейнера:
	```
	$ sudo docker container stop CONTAINER_ID
	```
## Решение ошибки “Error checking context on docker build”:
	```
	$ sudo chown root.root -R ../APP_NAME
	```
## Удаление неиспользуемых данных
	```
	$ docker system prune
	```
## Удаление неиспользуемых томов
	```
	$ docker volume prune
	```
