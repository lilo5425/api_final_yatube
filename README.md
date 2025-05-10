# Проект API для Yatube
REST API для социальной сети блогов с возможностью публикации записей, комментирования и подписки на авторов.

# Как запустить проект:

Cоздать и активировать виртуальное окружение:

python3 -m venv .venv


source .venv/bin/activate


Установить зависимости из файла requirements.txt:

python -m pip install --upgrade pip


pip install -r requirements.txt


Выполнить миграции:

python manage.py migrate


Запустить проект:

python manage.py runserver

# Примеры
- Публикация поста
```
POST /api/v1/posts/
{
    "text": "string"
}
```

- Получение постов постранично
```
GET /api/v1/posts/?limit=10&offset=10
```

- Получение всех комменатриев

```
GET /api/v1/posts/{post_id}/comments/
```

- Удаление комментария

```
DEL /api/v1/posts/{post_id}/comments/{comment_id}/
```
