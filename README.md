# django-modeltrans

[![CI](https://github.com/zostera/django-modeltrans/actions/workflows/ci.yml/badge.svg)](https://github.com/zostera/django-modeltrans/actions/workflows/ci.yml)
[![Documentation Status](https://readthedocs.org/projects/django-modeltrans/badge/?version=latest)](http://django-modeltrans.readthedocs.io/en/latest/?badge=latest)
[![Any color you like](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/ambv/black)

Translates Django model fields in a `JSONField` using a registration approach.

# Features/requirements

- Uses one PostgreSQL `jsonb`-field per model (via `django.db.models.JSONField`)
- Django 4.2, 5.0 (with their supported python versions)
- PostgreSQL >= 13 and the appropriate `psycopg` version for your Django version
- [Available on pypi](https://pypi.python.org/pypi/django-modeltrans)
- [Documentation](http://django-modeltrans.readthedocs.io/en/latest/)

# Running the tests

`tox`

Running the tests only for the current environment, use `make test`

# Attribution

Some concepts and code come from https://github.com/deschler/django-modeltranslation,
which is in turn inspired by https://github.com/zmathew/django-linguo

We started this solution at Zostera because we did not like:
 - The way django-modeltranslation adds one field per language (and thus requires a migration
when adding a language);
 - The unpredictability of the original field.

Since `JSONB` is supported by Postgres now, we developed this approach.

# Relevant 3rd party documentation

- [PostgreSQL jsonb functions](https://www.postgresql.org/docs/9.5/static/functions-json.html)
