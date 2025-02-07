# «API для Yatube»

## Описание проекта: 
Yatube - это простая соц.сеть, которая позволяет оставлять посты и комментарии к ним через API.

## Как запустить проект у себя:
Клонировать репозиторий и перейти в него в командной строке:
```
https://github.com/PotashevIlya/api_final_yatube
```
```
cd api_final_yatube
```
Cоздать и активировать виртуальное окружение:
```
python -m venv env
```
```
source venv/Scripts/activate
```
Установить зависимости из файла requirements.txt:
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python manage.py migrate
```
Запустить сервер:
```
python manage.py runserver
```
## Примеры запросов к API:
Полный список запросов можно получить по ссылке http://127.0.0.1:8000/redoc/ после запуска проекта. 

**GET:** http://127.0.0.1:8000/api/v1/posts/

<sub>Получить список всех публикаций. При указании параметров limit и offset выдача будет работать с пагинацией.</sub>
```
{
"id": 0,
"author": "string",
"text": "string",
"pub_date": "2024-08-02T14:15:22Z",
"image": "string",
"group": 0
}
```
**POST:** http://127.0.0.1:8000/api/v1/posts/

<sub>Добавление новой публикации в коллекцию публикаций. Анонимные запросы запрещены.</sub>
```
{
"text": "string",
"image": "string",
"group": 0
}
```
**POST:** http://127.0.0.1:8000/api/v1/posts/{id}/

<sub>Добавление нового комментария к публикации. Анонимные запросы запрещены.</sub>
```
{
"text": "string"
}
```
**POST:** http://127.0.0.1:8000/api/v1/follow/

<sub>Подписка пользователя от имени которого сделан запрос на пользователя переданного в теле запроса. Анонимные запросы запрещены.</sub>
```
{
"following": "string"
}
```
### Технологический стек :bulb:
- Языки и фреймворки  
  - python  
  - django  
  - djangorestframework

- Дополнительно установленные библиотеки Python  
  - djoser  
  - django_filters  
  - djangorestframework-simplejwt
  - requests
___  
#### Автор проекта:  
:small_orange_diamond: [Поташев Илья](https://github.com/PotashevIlya)  
