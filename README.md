# ⏰ Whenever-None

[![](https://img.shields.io/pypi/v/whenever-none.svg?color=blue)](https://pypi.python.org/pypi/whenever-none)
[![](https://img.shields.io/python/required-version-toml?tomlFilePath=https%3A%2F%2Fraw.githubusercontent.com%2FSuadeLabs%2Fwhenever-none%2Fmain%2Fpyproject.toml)](https://pypi.python.org/pypi/whenever-none)
[![](https://img.shields.io/pypi/l/whenever-none.svg?color=blue)](https://pypi.python.org/pypi/whenever-none)
[![](https://img.shields.io/github/actions/workflow/status/SuadeLabs/whenever-none/checks.yml?branch=main)](https://github.com/SuadeLabs/whenever-none)

**A slightly friendlier fork of whenever handling comparison with None**

This is a slightly niche fork of the excelent [whenever](https://github.com/ariebovenberg/whenever) library for handling comparison against null values. For our purposes, we count None as, essentially, year zero:

```python
>>> from whenever import Instance

>>> Instance.now() > None
True
```

You can install this library as a drop-in replacement without changing your code:

```sh
pip install whenever-none  # install this library
python -c "import whenever"  # use it like whenever
```

## Why use whenever-none?

If you want all the nice features of whenever, but often deal with poor quality data 💩 or data exploration 🔍, this library allows a lot of common python operations to proceed (e.g. sorting a list of Person instances by their `.bith_date` property) without requiring too much (or incorrect) massaging of the data.
