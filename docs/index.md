<div style="float: right">
    <a href="https://travis-ci.org/abetkin/webtypes"><img style="border: none; background-color: transparent; margin: 0" alt="Build Status" src="https://travis-ci.org/abetkin/webtypes.svg?branch=master"></a>
    <a href="https://codecov.io/gh/abetkin/webtypes"><img style="border: none; background-color: transparent; margin: 0" alt="codecov" src="https://codecov.io/gh/abetkin/webtypes/branch/master/graph/badge.svg"></a>
    <a href="https://pypi.python.org/pypi/webtypes"><img style="border: none; background-color: transparent; margin: 0" alt="Package version" src="https://badge.fury.io/py/webtypes.svg"></a>
</div>

# webtypes

This is a fork of [API Star](https://github.com/encode/apistar) 0.5.*

<!-- [![Build Status](https://travis-ci.org/abetkin/webtypes.svg?branch=master)](https://travis-ci.org/abetkin/webtypes)
[![codecov](https://codecov.io/gh/abetkin/webtypes/branch/master/graph/badge.svg)](https://codecov.io/gh/abetkin/webtypes)
[![Package version](https://badge.fury.io/py/webtypes.svg)](https://pypi.python.org/pypi/webtypes) -->

**Community:** [https://discuss.apistar.org/](https://discuss.apistar.org/) 🤔 💭 🤓 💬 😎

**Repository**: [https://github.com/abetkin/webtypes](https://github.com/abetkin/webtypes) 💻

---

## Quickstart

Install API Star:

```bash
$ pip3 install webtypes
```

Create a new project in `app.py`:

```python
from webtypes import App, Route


def welcome(name=None):
    if name is None:
        return {'message': 'Welcome to API Star!'}
    return {'message': 'Welcome to API Star, %s!' % name}


routes = [
    Route('/', method='GET', handler=welcome),
]

app = App(routes=routes)


if __name__ == '__main__':
    app.serve('127.0.0.1', 5000, debug=True)
```

Open `http://127.0.0.1:5000/docs/` in your browser:

![API documentation](img/api-docs.png)
