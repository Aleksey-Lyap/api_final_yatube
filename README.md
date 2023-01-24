### Описание проекта «API для Yatube»:
API-сервис Yatube может использоваться для взаимодействия с другими приложениями и сервисами.
Доступ к контенту сайта  частично ограничен: смотреть информацию о постах могут любые посльзователи, а создавать публикации и подписываться на авторов только авторизованые пользователи.

### Как запустить проект:
Клонировать репозиторий и перейти в него в командной строке:
```
git clone https://github.com/Aleksey-Lyap/api_final_yatube.git
```
Cоздать и активировать виртуальное окружение:
```
python3 -m venv venv
```
```
source venv/bin/activate
```
Установить зависимости из файла requirements.txt:
```
python3 -m pip install --upgrade pip
```
```
pip install -r requirements.txt
```
Выполнить миграции:
```
python3 manage.py migrate
```
Запустить проект:
```
python3 manage.py runserver
```

### Примеры запросов к API:
__GET__ _http://127.0.0.1:8000/api/v1/posts/_
```
_Response samples:_
{
"count": 123,
"next": "http://api.example.org/accounts/?offset=400&limit=100",
"previous": "http://api.example.org/accounts/?offset=200&limit=100",
"results": [{}]
}
```
__POST__ _http://127.0.0.1:8000/api/v1/posts/{post_id}/comments/_
```
Request samples:
{
"text": "string"
}
```
```
Response samples:
{
"id": 0,
"author": "string",
"text": "string",
"created": "2019-08-24T14:15:22Z",
"post": 0
}
```
