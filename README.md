# docker-help
Заметки по использованию docker на Ubuntu 18.04 LTS
# Список активных и неактивных контейнеров:
	```
	$ sudo docker container ls -a
	```
# Запуск имеджа:
	```
	$ sudo docker run IMAGE_NAME
	```
# Билдинг имеджа с использованием тега, по которому позже его можно будет запускать. Имедж сбилдится только в том случае, если в директории есть Dockerfile:
	```
	$ sudo docker build -t YOUR_TAG_NAME .
	```
# Запуск имеджа с пробросом портов на хостовую машину:
	```
	$ sudo docker run -p 4000:80 IMAGE_NAME
	```
# Запуск в Detached-mode:
	```
	$ sudo docker run -d -p 4000:80 IMAGE_NAME
	```
# Остановка контейнера:
	```
	$ sudo docker container stop CONTAINER_ID
	```
# Решение ошибки “Error checking context on docker build”:
	```
	$ sudo chown root.root -R ../APP_NAME
	```
