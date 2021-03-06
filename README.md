<p align="center">
    <img src="https://raw.githubusercontent.com/abetkin/webtypes/master/docs/img/logo-200-square-light.png" alt="webtypes" />
</p>
<p align="center">
    <em>A smart Web API framework, for Python 3.</em>
</p>
<p align="center">
<a href="https://travis-ci.org/abetkin/webtypes">
    <img src="https://travis-ci.org/abetkin/webtypes.svg?branch=master" alt="Build Status">
</a>
<a href="https://codecov.io/gh/abetkin/webtypes">
    <img src="https://codecov.io/gh/abetkin/webtypes/branch/master/graph/badge.svg" alt="codecov">
</a>
<a href="https://pypi.python.org/pypi/webtypes">
    <img src="https://badge.fury.io/py/webtypes.svg" alt="Package version">
</a>
</p>

---

**Community:** https://discuss.apistar.org 🤔 💭 🤓 💬 😎

**Documentation:** https://abetkin.github.io/webtypes 📘

---

# Features

Why might you consider using webtypes for your next Web API project?

* **Schema generation** - Support for automatically generating OpenAPI schemas.
* **Expressive** - Type annotated views, that make for expressive, testable code.
* **Performance** - Dynamic behaviour for determining how to run each view makes webtypes incredibly efficient.
* **Throughput** - Support for asyncio allows for building high-throughput non-blocking applications.

---

# Quickstart

Install webtypes:

```bash
$ pip3 install webtypes
```

Create a new project in `app.py`:

```python
from webtypes import App, Route


def welcome(name=None):
    if name is None:
        return {'message': 'Welcome to webtypes!'}
    return {'message': 'Welcome to webtypes, %s!' % name}


routes = [
    Route('/', method='GET', handler=welcome),
]

app = App(routes=routes)


if __name__ == '__main__':
    app.serve('127.0.0.1', 5000, debug=True)
```

Open `http://127.0.0.1:5000/docs/` in your browser:

![API documentation](https://raw.githubusercontent.com/abetkin/webtypes/master/docs/img/api-docs.png)

---

<p align="center"><i>webtypes is <a href="https://github.com/tomchristie/webtypes/blob/master/LICENSE.md">BSD licensed</a> code.</i>
<p align="center">
    <img src="https://raw.githubusercontent.com/abetkin/webtypes/master/docs/img/ident-44-square-light.png" alt="webtypes" />
</p>
