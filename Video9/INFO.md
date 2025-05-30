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

# Video 5 - Part 1

django-silk for Profiling and Optimization with Django REST Framework
[https://www.youtube.com/watch?v=OG8alXR4bEs&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=5]

django-silk
[https://github.com/jazzband/django-silk]

```
$ pip install django-silk
$ pip freeze > requirements.txt

File: drf_course/settings.py
MIDDLEWARE = [
    ...
    'silk.middleware.SilkyMiddleware',
    ...
]

INSTALLED_APPS = (
    ...
    'silk',
)

File: drf_course/urls.py
urlpatterns = [
    ...
    path('silk/', include('silk.urls', namespace='silk'))
]

$ python manage.py migrate
```

# Video 6 - Part 1

Django REST Framework - Generic Views | ListAPIView & RetrieveAPIView
[https://www.youtube.com/watch?v=vExjSChWPWg&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=6]

Generic Views
[https://www.django-rest-framework.org/api-guide/generic-views/]

# Video 6 - Part 2

...

# Video 7 - Part 1

Django REST Framework - Dynamic Filtering | Overriding get_queryset() method
[https://www.youtube.com/watch?v=3Gi-w4Swge8&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=7]

```
$ python mange.py createsuperuser
User: ubuntuuser
Password: u***r
```

# Video 7 - Part 2

...

# Video 8 - Part 1

Django REST Framework - Permissions and Testing Permissions
[https://www.youtube.com/watch?v=rx5IV_4Iuog&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=8]

# Video 9 - Part 1

Django REST Framework - APIView class
[https://www.youtube.com/watch?v=TVFCU0w65Ak&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=9]

