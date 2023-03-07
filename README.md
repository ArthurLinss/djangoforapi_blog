# DjangoForAPI Blog Tutorial


# Setup

Note that there is lower django version used here due to incompatabilities with dj-rest-auth and get_lazy.
```
pip install -r requirements.txt
```

# Scheme
Create static scheme:
```
pip install pyaml uritemplate
python manage.py generateschema > openapi-schema.yml
```

Dynamic scheme implemented via urls:
```
from rest_framework.schemas import get_schema_view # new

path('openapi', get_schema_view(
title="Blog API",
description="A sample API for learning DRF",
version="1.0.0"
), name='openapi-schema'),
```
Go to:
```
http://127.0.0.1:8000/openapi
```

# Documentation

```
pip install drf-yasg
```
See main urls.py file for more.
Paths to check:
```
http://127.0.0.1:8000/swagger/
http://127.0.0.1:8000/redoc/
```


# Literature

Rest tutorial: `https://learndjango.com/tutorials/official-django-rest-framework-tutorial-beginners`
