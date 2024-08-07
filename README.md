# «API для Yatube»

## Описание проекта: 
Yatube - это простая соц.сеть, которая позволяет оставлять посты и комментарии к ним через API. Благодаря этому проекту я ознакомился с основными принципами работы API как в теории, так и на практике.

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
python3 manage.py runserver
```
С этого момента вы можете отправлять запросы к API!
