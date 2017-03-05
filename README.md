# VK API

This is an ultimate library for **vk.com** API written in Python.

## Installation
Just: 
```bash
git clone https://github.com/ISosnovik/vkAPI
cd vkAPI
python setup.py install
```

## General use

To begin with:

```python
from vkapi.methods import *
```

You can use it exactly as it is described [here](https://vk.com/dev/methods).
For example:

```python
users.get(user_ids=1, fields='city')
#[{'city': 2, 'first_name': 'Pavel', 'last_name': 'Durov', 'uid': 1}]
```

## Access Token

Some methods use `access_token`. It shouldn't be passed as a parameter to method. Nevertheless, it is defined as a global variable `ACCESS_TOKEN` in `vkapi.vkapi` module. Just set it at the beginnig:
 
```python
import vkapi

vkapi.ACCESS_TOKEN = 'h3r3-1s-th3-4cc3ss-t0k3n'
```
And that is it. The rest is the same as it was before. 

## Documentation

All methods are provided with short description and reference to the official documentation. If you forget something, just call `help` or `shift + tab + tab` for *__Jupyter Notebook__* and you will get the description:

```profile
Help on function resolveScreenName in module vkapi.methods.utils:

resolveScreenName(screen_name=None)
    Detects a type of object (e.g., user, community, application)
    and its ID by screen name.
    https://vk.com/dev/utils.resolveScreenName
```