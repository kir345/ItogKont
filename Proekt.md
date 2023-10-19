# Контейнеризация
**Кузнецов К.Ю. Итоговый проект**

## Задание

1. Cоздать сервис, состоящий из 2 различных контейнеров: 

1 - веб, 

2 - БД (compose).

Для выполнения первого задания использовались следующие команды:

* docker run --name some-mysgl -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:8.0.31;

![](/3.png)

* docker run --name myphp -d --link some-mysql:db -p 8081:80 phpmyadmin/phpmyadmin;

![](/5.png)

* docker ps -a

![](/7.png)

Для второго:

* mkdir folderforcompose

* ls, cd folderforcompose

![](/11.png)

* sudo nano docker-compose.yml
Здесь указываем версию синтаксиса файла docker-compose, описываем сервисы, которые будут запущены

![](/9.png)

* cat docker-compose.yml

![](/12.png)

* docker-compose up -d

![](/14.png)

* docker ps -a

![](/15.png)



