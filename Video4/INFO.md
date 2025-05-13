# drf-course-api3

Django REST Framework Series
[https://www.youtube.com/playlist?list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t]

# Video 1 - Part 1

Django REST Framework series - Setup and Models
[https://www.youtube.com/watch?v=6AEvlNgRPNc&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=1]

```
$ python3 -m venv venv-drf
$ source venv-drf/bin/activate
$ pip install -r requirements.txt
```

# Video 1 - Part 2

```
$ python manage.py populate_db

$ python manage.py graph_models api > models.dot
```

# Video 2 - Part 1

Django REST Framework - Serializers & Response objects | Browsable API
[https://www.youtube.com/watch?v=BMym71Dwox0&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=2]

Installation
[https://www.django-rest-framework.org/#installation]

Serializers
[https://www.django-rest-framework.org/api-guide/serializers/]

Serializers#Validation
[https://www.django-rest-framework.org/api-guide/serializers/#validation]

Serializer fields
[https://www.django-rest-framework.org/api-guide/fields/]

The Browsable API
[https://www.django-rest-framework.org/topics/browsable-api/]

Local
[http://localhost:8000/products/?format=json]
[http://localhost:8000/products/?format=api]
[http://localhost:8000/products/1/]

```
File: drf_course/settings.py
INSTALLED_APPS = [
    ...
    'rest_framework',
]
```

# Video 3 - Part 1

Django REST Framework- Nested Serializers, SerializerMethodField and Serializer Relations
[https://www.youtube.com/watch?v=KfSYadIFHgY&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=3]

Serializer relations
[https://www.django-rest-framework.org/api-guide/relations/]


# Video 3 - Part 2

 ...

# Video 4 - Part 1

Django REST Framework - Serializer subclasses and Aggregated API data
[https://www.youtube.com/watch?v=_xbI0-mjtw4&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=4]

