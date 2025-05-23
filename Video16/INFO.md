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

# Video 10 - Part 1

Django REST Framework - Creating Data | ListCreateAPIView and Generic View Internals
[https://www.youtube.com/watch?v=Jh85U1nhMh8&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=10]

# Video 10 - Part 2

Classy Django REST Framework
[https://www.cdrf.co/]

# Video 11 - Part 1

Django REST Framework - Customising permissions in Generic Views | VSCode REST Client extension
[https://www.youtube.com/watch?v=mlQZ1i8rUKQ&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=11]

Install REST Client Extension

# Video 12 - Part 1

Django REST Framework - JWT Authentication with djangorestframework-simplejwt
[https://www.youtube.com/watch?v=Xp0-Yy5ow5k&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=12]

TokenAuthentication
[https://www.django-rest-framework.org/api-guide/authentication/#tokenauthentication]

JSON Web Token Authentication
[https://www.django-rest-framework.org/api-guide/authentication/#json-web-token-authentication]

github jazzband/djangorestframework-simplejwt
[https://github.com/jazzband/djangorestframework-simplejwt]

Simple JWT
[https://django-rest-framework-simplejwt.readthedocs.io/en/latest/]

```
File: drf_course/settings.py
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework.authentication.BasicAuthentication',
        'rest_framework.authentication.SessionAuthentication',
    ]
}
```

# Video 12 - Part 2

```
$ pip install djangorestframework-simplejwt
$ pip freeze > requirements.txt

File: drf_course/settings.py
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework.authentication.SessionAuthentication',
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ]
}

File: drf_course/urls.py
...
from rest_framework_simplejwt.views import (
    TokenObtainPairView,
    TokenRefreshView,
)

urlpatterns = [
    ...
    path('api/token/', TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', TokenRefreshView.as_view(), name='token_refresh'),
]
```

JSON Web Token (JWT) Debugger
[https://jwt.io/]

## Video 12 - Part 3

...

## Video 13 - Part 1

Django REST Framework - Refresh Tokens & JWT Authentication
[https://www.youtube.com/watch?v=H3OY36wa7Cs&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=13]

## Video 14 - Part 1

Django REST Framework - Updating & Deleting data
[https://www.youtube.com/watch?v=08gHVFPFuBU&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=14]

## Video 14 - Part 2

...

## Video 15 - Part 1

drf-spectacular - Django REST Framework API Documentation
[https://www.youtube.com/watch?v=E3LUvsPWLwM&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=15]

tfranzel/drf-spectacular
[https://github.com/tfranzel/drf-spectacular]

## Video 15 - Part 2

```
$ pip install drf-spectacular
$ pip freeze > requirements.txt

File: drf_course/settings.py
INSTALLED_APPS = [
    # ALL YOUR APPS
    'drf_spectacular',
]

REST_FRAMEWORK = {
    # YOUR SETTINGS
    'DEFAULT_SCHEMA_CLASS': 'drf_spectacular.openapi.AutoSchema',
}

SPECTACULAR_SETTINGS = {
    'TITLE': 'E-Commerce API',
    'DESCRIPTION': 'A simple Product & Order API that helps you learn Django Rest Framework',
    'VERSION': '1.0.0',
    'SERVE_INCLUDE_SCHEMA': False,
    # OTHER SETTINGS
}

$ python manage.py spectacular --color --file schema.yml

File: drf_course/urls.py
urlpatterns = [
    ...

    # YOUR PATTERNS
    path('api/schema/', SpectacularAPIView.as_view(), name='schema'),
    # Optional UI:
    path('api/schema/swagger-ui/', SpectacularSwaggerView.as_view(url_name='schema'), name='swagger-ui'),
    path('api/schema/redoc/', SpectacularRedocView.as_view(url_name='schema'), name='redoc'),
]

```

Local
[http://localhost:8000/api]
[http://localhost:8000/api/schema/swagger-ui/]
[http://localhost:8000/api/schema/redoc/]

## Video 16 - Part 1

django-filter and DRF API filtering - Django REST Framework
[https://www.youtube.com/watch?v=NDFgTGTI8zg&list=PL-2EBeDYMIbTLulc9FSoAXhbmXpLq2l5t&index=16]

[https://www.django-rest-framework.org/api-guide/filtering/]

```
$ pip install django-filter
$ pip freeze > requirements.txt 

File: drf_course/settings.py
INSTALLED_APPS = [
    ...
    'django_filters',
]

REST_FRAMEWORK = {
    ...
    'DEFAULT_FILTER_BACKENDS': ['django_filters.rest_framework.DjangoFilterBackend'],
}
```

Local
[http://localhost:8000/products/?name=Television]
[http://localhost:8000/products/?price=300]
[http://localhost:8000/products/?price__gt=100]
[http://localhost:8000/products/?price__lt=100]
[http://localhost:8000/products/?price__range=100,350]

