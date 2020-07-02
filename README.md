# Яндекс.Практикум
  
## Проектная работа 15_v1.0.2
 
## Backend deployment

### Краткая информация о проекте

Создание удаленного сервера, привязка домена и развертка на сервере приложения для работы с проектом Mesto.
В работе применяются базы данных MongoDB для разработки бэкенда проекта Mesto и разработки API, согласно принципам REST.

### Ссылки

- Фронтенд проекта доступен по адресам:
  - [mesto-updated.tk](https://mesto-updated.tk)
  - [www.mesto-updated.tk](https://www.mesto-updated.tk) 
- Бэкенд проекта доступен по адресам: 
  - [api.mesto-updated.tk](https://api.mesto-updated.tk)
  - [www.api.mesto-updated.tk](https://www.api.mesto-updated.tk)
  - [84.201.159.37](http://84.201.159.37/)

### ПО для выполнения задания:

<li>
Git
<li>
Node.js
<li>
MongoDB
<li>
NPM-пакеты:

eslint, eslint-config-airbnb-base, eslint-plugin-import, express, mongoose, body-parser, validator, bcryptjs, jsonwebtoken, dotenv, helmet celebrate joi winston express-winston
  

### Инструкция по сборке:
- бекенд на сервере запускается командой **pm2 start app.js**
- при отправке запросов через **Postman** в заголовок **authorization** нужно записать схему аутентификации (используем **Bearer**) и токен через пробел: 

  - **POST/signup** создаёт пользователя. В теле POST-запроса на создание пользователя передается JSON-объект с пятью полями: **name**, **about**, **avatar**, **email**, **password**
  - **POST/signin** производит авторизацию пользователя. Если успешно - токен возвращается в ответе и записыватеся в cookie с включенной опцией httpOnly. В теле POST-запроса на создание пользователя передается JSON-объект с двумя полями: **email**, **password**
  
  - **GET/users** возвращает всех пользователей из базы
  - **GET/users/:userId** возвращает конкретного пользователя
  - **GET/cards** возвращает все карточки всех пользователей
  - **POST/cards** создаёт карточку. В теле POST-запроса на создание карточки передается JSON-объект с двумя полями: **name** и **link**.
  - **DELETE/cards/:cardId** удаляет карточку по идентификатору
  - **PATCH/users/me** — обновляет профиль
  - **PATCH/users/me/avatar** — обновляет аватар
  - **PUT/cards/:cardId/likes** — поставить лайк карточке
  - **DELETE/cards/:cardId/likes** — убрать лайк с карточки
 
  
### Итоги проектной работы:

- создан бесплатный удаленный сервер на базе [Яндекс Облако](https://cloud.yandex.ru). К серверу привязаны домен и субдомены
- на сервере развернут фронтенд и бекенд проекта Место
- сервер отвечает на запросы и отдает фронтенд проекта Место при обращении по раздельным адресам
- ошибки сервера обрабатываются централизовано
