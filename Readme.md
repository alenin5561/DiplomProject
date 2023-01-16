# Дипломный проект по профессии «Тестировщик» 

Дипломный проект — автоматизация тестирования комплексного сервиса, взаимодействующего с СУБД и API Банка.

## Необходимое окружение:
- Java 11
- Docker
- IntelliJ IDEA
- Chrome бразуер версии 108.0.5359.125 
- Удостовериться что порты 8080, 9999 и 5432 или 3306 свободны.

* Сервис в браузере должен открыться на порту 8080.
по ссылке http://localhost:8080/

Найти запущенный процес/порт:

` netstat -a ` 

## Инструкция по установке:
- Склонируйте репозиторий 
- Поднимите контейнеры командой `docker compose up `
- Запустите приложение с сервисом , указав предварительно путь к файлу  ` java -jar artifacts/aqa-shop.jar `
- Для запуска сервиса с взаимодействием с базами данных прописываем в терминале следующие команды:

для mysql ` java "-Dspring.datasource.url=jdbc:mysql://localhost:3306/app" -jar artifacts/aqa-shop.jar `

для postgresql ` java "-Dspring.datasource.url=jdbc:postgresql://localhost:5432/app" -jar artifacts/aqa-shop.jar `
