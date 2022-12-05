# Docker

- <a href="#1">Загрузка образа</a>
- <a href="#2">Просмотр образов (Images)</a>
- <a href="#3">Запуск контейнера</a>
- <a href="#4">Просмотр контейнеров</a>
- <a href="#5">Остановка и удаление контейнеров</a>
- <a href="#6">Работа с терминалом из под ubuntu</a>
- <a href="#7">Запуск ранее созданного контейнера</a>
- <a href="#8">Выполнение команды внутри запущенного контейнера</a>
- <a href="#9">Создание образа из Dockerfile</a>
- <a href="#10">Запуск docker-compose</a>
- <a href="#11">Остановка docker-compose</a>

> **<div id="1">Загрузка образа</div>** <br>Пример:
>> docker pull `<IMAGE_NAME>` <br>
>> docker pull ubuntu:18.10  <br>
>> или <br>
>> docker pull ubuntu:latest (latest - последняя версия)
> 
> **<div id="2">Просмотр образов (Images)</div>** <br>Пример:
>> docker images
>
> **<div id="3">Запуск контейнера</div>** <br>Пример:
>> docker run `<IMAGE> <Опциональная команда, которая выполнится внутри контейнера>` <br>
>> docker pull ubuntu:18.10 echo "hello from ubuntu"
> 
> **<div id="4">Просмотр контейнеров</div>** <br>Пример:
>> docker ps _(Запущенные контейнеры)_ <br>
>> docker ps -a (_Все существующие контейнеры_)
> 
> **<div id="5">Остановка и удаление контейнеров</div>** <br>Пример:
>> docker stop `<CONTAINER_ID>` <br>
>> docker rm `<CONTAINER_ID>` <br>
>> docker stop 79c6b7c <br>
>> docker rm 79c6b7c <br>
>> `Что бы после выполнения команды контейнер удалялся используйте --rm, Пример:` <br>
>> docker run -it --rm ubuntu:18.10 /bin/bash
> 
> **<div id="6">Работа с терминалом из под ubuntu</div>** <br>Пример:
>> docker run -it ubuntu:18.10 /bin/bash <br>
>> docker run -i -t ubuntu:18.10 /bin/bash <br>
>> docker run -t -i ubuntu:18.10 /bin/bash <br>
>> `Опция -it вмсете с /bin/bash дает доступ к терминалу exit выход из терминала`
> 
> **<div id="7">Запуск ранее созданного контейнера</div>** <br>Пример:
>> docker start `<CONTAINER_ID>` <br>
>> docker start 79c6b7c
> 
> **<div id="8">Выполнение команды внутри запущенного контейнера</div>** <br>Пример:
>> docker exec -it 79c6b7c /bin/bash `для запуска внутри контейнера используется exec`
> 
> **<div id="9">Создание образа из Dockerfile</div>** <br>Пример:
>> docker build `<DOCKERFILE_PATH>` --tag `<IMAGE_NAME>` (`если точка то будет выбрата текущая дирректория`) <br>
>> docker build . --tag myImage
>
> **<div id="10">Запуск docker-compose</div>** <br>Пример:
>> docker-compose up -d
> 
> **<div id="10">Остановить docker-compose</div>** <br>Пример:
>> docker-compose down