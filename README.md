# Outline Web Manager


Написанная на Python Веб-морда для [Outline VPN](https://getoutline.org/)

### Предупреждение

Написана для личного пользования. Фронт написан за HTML POST-запросах с использованием фрёмворка Bootstrap, никакие другие фреймворки на JS не использовались. Бэкэнд на Python FastAPI приложение написано при помози библиотеки [outline-vpn-api](https://github.com/jadolg/outline-vpn-api) чтобы работать с Outline Server менеджер API.
### Скриншоты

<img width="500" alt="screenshot.png from repo" src="https://user-images.githubusercontent.com/18418712/213498267-46aaabd0-61f8-4c97-83ca-21a8d99a1ddd.png">

### Требования

1.docker 
2.docker-compose

## Как использовать

Установите Outline Server как положено. В ответ даст вам ключ вида:
```
{"apiUrl":"https://76.117.122.22:11384/Psq45dRf4fK34fZpS249Kj","certSha256":"A227C34FB165B0444105154B615F6E2DA1221A7A30C749869B2CE32F98F22654"}
```

Запустите docker container из этого репозитория (Это автоматически построит образ и т.д.):
```
docker-compose up
```


После всего это вы получите доступ с http://<ваш_айпи>:8000.


Пожалуйста введите этот ключ из установщика сервера в поле ввода и потвердите свои намерения.

Сервер сохранит предоставленные учетные данные в файлах cookie вашего браузера (не хранит учетные данные на сервере) и даст вам полный доступ к веб-морде менеджера: 
1) Получение списка ключей;
2) Получать \Редактировать информацию о сервере;
3) Добавлять \ Переименовывать \ Удалять ключи;
4) Устанавливать \ Удалять лимиты использования данных на всех ваших ключах;
5) Устанавливать \ Удалять лимиты использования данных для каждого ключа отдельно (индивидуально);
6) Включать \ Выключать анонимную статистику.
