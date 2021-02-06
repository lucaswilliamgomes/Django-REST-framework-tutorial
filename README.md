# Django REST framework tutorial

This tutorial will cover creating a simple pastebin code highlighting Web API. Along the way it will introduce the various components that make up REST framework, and give you a comprehensive understanding of how everything fits together.

## []()Getting Started

### []()Prerequisites

```
Python3
Pip
Python virtualenv
Django
Django Rest Framework
```

Activate your virtual environment before proceeding with the installation.

### []()Installing

To install the requirements:

```
pip install -r requirements.txt
```

To do database migrations:

```
python manage.py migrate
python manage.py makemigrations
```

## []()Running the Rest API

To run the Rest API:

```
python manage.py runserver
```

> Access in: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## []()Built With

- [Django Rest Framework](https://www.django-rest-framework.org/)

## Create authenticated user 
```
python manage.py createsuperuser
```

# REST API

The REST API is described below.

## All API endpoints:

- GET: `/` - API root
- GET: `/users` - List all users
- GET: `/snippets` - List all snippets
- POST: `/snippets` - Creates an authenticated-only snippet.
- GET/PUT/DELETE: `/snippets/<id>` - PUT and DELETE only for the authenticated user who created the snippet. Get, delete or update snippet.
- GET: `/snippets/<id>/highlight` - Get HTML representations of the featured snippet.

## How to use API endpoints

## List all users

#### Method:

- GET: `/users`

#### URL Example:

> [http://127.0.0.1:8000/users/](http://127.0.0.1:8000/users/)

JSON example User:

```json
{
    "url": "http://127.0.0.1:8000/users/1/",
    "id": 1,
    "username": "lucas",
    "snippets": [
        "http://127.0.0.1:8000/snippets/1/",
        "http://127.0.0.1:8000/snippets/2/",
        "http://127.0.0.1:8000/snippets/3/",
        "http://127.0.0.1:8000/snippets/4/",
        "http://127.0.0.1:8000/snippets/5/"
    ]
}
```
---
## List all snippets

#### Method:

- GET: `/snippets`

#### URL Example:

> [http://127.0.0.1:8000/snippets/](http://127.0.0.1:8000/snippets/)

---
## Add snippet

#### Method:

- POST: `/snippets/`

#### URL Example

> [http://127.0.0.1:8000/snippets/](http://127.0.0.1:8000/snippets/)

JSON example snippet:

```json
{
    "url": "http://127.0.0.1:8000/snippets/6/",
    "id": 6,
    "highlight": "http://127.0.0.1:8000/snippets/6/highlight/",
    "owner": "lucas",
    "title": "hello world",
    "code": "cout << \"hello world\" << endl;",
    "linenos": false,
    "language": "c++",
    "style": "abap"
}
```
---
## Get snippet

#### Method

- GET: `/snippets/<id>`
  - `<id> is the identifier of the snippet.`

#### URL Example:

> [http://127.0.0.1:8000/snippets/1/](http://127.0.0.1:8000/snippets/1/)

---
## Update snippet

#### Method

- PUT: `/snippets/<id>/`
  - `<id> is the identifier of the snippet.`

#### URL example:

> [http://127.0.0.1:8000/snippets/1/](http://127.0.0.1:8000/snippets/1/)
---
## Delete snippet

#### Method

- DELETE: `/snippets/<id>/`
  - `<id> is the identifier of the snippet.`

#### URL example:

> [http://127.0.0.1:8000/snippets/1/](http://127.0.0.1:8000/snippets/1/)
---
## Highlight snippet

#### Method

- GET: `/snippets/<id>/highlight`
  - `<id> is the identifier of the snippet.`

#### URL example:

> [http://127.0.0.1:8000/snippets/1/highlight](http://127.0.0.1:8000/snippets/1/highlight)
---

## Authors

- [**Lucas William Gomes**](https://github.com/lucaswilliamgomes)

