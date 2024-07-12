# Django Cotton Components

<https://django-cotton.com/docs/>

## Install

```shell
pip install django-cotton
```

```python
# settings.py
INSTALLED_APPS = [
    ...
    'django_cotton',
]

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': ['your_project/templates'], # Add your template directories here
        'APP_DIRS': False,
        'OPTIONS': {
            'loaders': [
                'django_cotton.cotton_loader.Loader', # First position
                # continue with default loaders, typically:
                # "django.template.loaders.filesystem.Loader",
                # "django.template.loaders.app_directories.Loader",
            ],
            'builtins': [
                'django_cotton.templatetags.cotton',
            ],
        },
    },
]
```

Create components in `templates/cotton/.`
