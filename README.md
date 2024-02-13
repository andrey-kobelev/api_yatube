# API Yatube  
### Автор
- Кобелев Андрей Андреевич
- andrey.pydev@gmail.com
  
---  

## Краткое описание

**Yatube** — это платформа для блогов. 

**Возможности Yatube:**
- Зарегистрироваться;
- Создать, отредактировать или удалить собственный пост;
- Прокомментировать пост другого автора и подписаться на него.  

## Как запустить проект:

Клонировать репозиторий и перейти в него в командной строке:

```
git clone https://github.com/andrey-kobelev/api_final_yatube.git
```

```
cd api_final_yatube
```

Cоздать и активировать виртуальное окружение:

```
python3 -m venv env
```

```
source env/bin/activate
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

## Документация для API Yatube

Когда вы запустите проект, будет доступна [документация](http://127.0.0.1:8000/redoc/) для API **Yatube**.  Документация представлена в формате **Redoc**.

## Примеры запроса и ответа

### Получение публикаций
Получить список всех публикаций. При указании параметров `limit` и `offset` выдача должна работать с пагинацией.

Сделайте GET-запрос на адрес:

http://127.0.0.1:8000/api/v1/posts/

Вывод будет таким:

```json
[
    {    
	    "id": 0,
	    "author": "string",
	    "text": "string",
	    "pub_date": "2021-10-14T20:41:29.648Z",
	    "image": "string",
	    "group": 0
    }
]

```

## Технологии
- [Python](https://www.python.org/)
- [Django REST Framework](https://www.django-rest-framework.org/)
- [Simple JWT](https://django-rest-framework-simplejwt.readthedocs.io/en/latest/)
- [Djoser](https://djoser.readthedocs.io/en/latest/getting_started.html)