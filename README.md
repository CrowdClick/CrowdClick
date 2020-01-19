# CrowdClick

[![Build Status](https://travis-ci.com/CrowdClick/CrowdClick.svg?branch=master)](https://travis-ci.com/CrowdClick/CrowdClick)
[![codecov](https://codecov.io/gh/CrowdClick/CrowdClick/branch/master/graph/badge.svg)](https://codecov.io/gh/CrowdClick/CrowdClick)

Backend of affordable solution that combines traffic and quantitative data to the advertiser
through a crowd-sourcing click to view reward model


## Install and run project

```bash
# Create virtual environment
# https://virtualenvwrapper.readthedocs.io/en/latest/
mkvirtualenv -p python3.6 -a . crowdclick

# Install dependencies
pip install -r requirements.txt

# Initialize local settings
echo 'from .defaults import *' > crowdclick/settings/local.py

# Run migrations
python manage.py migrate

# Load initial data
python manage.py loaddata ad_source/fixtures/*

# Run server
python manage.py runserver 0.0.0.0:8000
```

You should see API endpoints on [http://localhost:8000/api/](http://localhost:8000/api/)

## Check code quality

```bash
# Run tests
python manage.py test

# Flake8
pip install flake8 && flake8 .
```

## Contributions

Contributions are welcome. Be sure to check our
[Code of conduct](https://github.com/CrowdClick/.github/blob/master/CODE_OF_CONDUCT.md)

## Licence

[MIT](https://github.com/CrowdClick/CrowdClick/blob/master/LICENCE)
