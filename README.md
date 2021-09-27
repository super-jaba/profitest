# URL Shortener Описание API

  * # Установка
    1. В корневой директории создать файл .env, в котором необходимо указать следующие параметры:
        * **PROTOCOL** (по умолчанию http)
        * **DOMAIN** (по умолчанию localhost)
        * **PORT** (по умолчанию 5000)
        * **DB_URI** - ссылка для подключения к _созданной_ базе данных MongoDB
        * При успешном запуске сервер выведет в терминал порт сервера и уведомление об успешном подключении к MongoDB
        
    2. Открыть в корневой директории терминал и выполнить следующую команду: _**npm run server**_
    
 * # Описание работы API
   #### Сервер обрабатывает 3 ссылки:
      * _**'/'**_ (GET) - декоративный запрос
      * _**'/new'**_ (POST) - запрос, создающий новую короткую ссылку
        > В теле **body** принимает обязательный параметр _'url'_, в котором передается исходная ссылка и опциональный _'custom'_ (должен быть уникальным), в котором можно указать желаемый вид короткой ссылки
      * _**'/:url'**_ (GET) с параметром _url_ - осуществляет редирект по заранее созданной ссылке


