# Тестовое задание на PHP Yii2 разработчика

## Задание

Создать проект на yii2 с использованием docker-compose.
в папке с проектом должен быть скрипт deploy.sh, который разворачивает готовый к работе локальный сайт (должен
заработать на linux).

## Стек

- БД - PostgresSQL
- Веб-сервер - Nginx
- Фреймворк - Yii2

## Страницы

### Главная страница

На странице появляется случайная фотография с сайта https://picsum.photos/

Фото получается по url https://picsum.photos/id/1020/600/500 где:

- 1020 - в url это id фотки
- 600 и 500 - это размеры фотки (неважно какие)

Под фотографией располагаются 2 кнопки: отклонить и одобрить.
При нажатии на любую из кнопок соответствующий запрос отправляется на сервер асинхронно.
k
Затем появляется новая фотография и так по кругу.

Фотографии по которым было принято решение больше не показываются.

### Админская страница

Доступ к странице предоставляется только при наличии токена xyz123 в get параметре.

На странице выводится таблица со следующими столбцами:

- id фотографии который является ссылкой на эту фотографию
- решение - одобрена или отклонена
- кнопка отмены решения (можно синхронно)
