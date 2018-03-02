# AsictCert

Asictcert is a Django package that contains an api called "AsictApi". This api help an edx instance to share information (like courses, certificates ..) with a trusted client using a JSON response. 



## How to install AsictApi

### Install the package
In the edxapp venvs run:

```bash
pip install git+https://github.com/PolimiOpenKnowledge/asictcert.git
```

### Register the application

Add the application to `INSTALLED_APPS` setting :

```python
INSTALLED_APPS = (
    ...
    'asictapi'
)
```

### URLs entries

Add URLs entries:

```python
urlpatterns = patterns('',
    ...
    url(r'', include('oai.urls')),
    url(r'^asictapi/', include('asictapi.urls')),
    ...
)
