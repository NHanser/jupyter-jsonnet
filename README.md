Jupyter-Jsonnet
===============

This package provides a Jupyter Kernel to support the Jsonnet language.  It is
based on the official Jsonnet language bindings.

After installing it, you need to register it to Jupyter with the command:
```sh
python3 -m jupyter_jsonnet.post_install
```

This kernel extends jsonnet syntax slightly to permit

* Cells containing only statements (These produce no result, but are checked
  for errrors).
* Definitions (statements) from previous cells to carry over, even if the cell
  containing the definition produced a result.

The parsing to separate statements from expressions is very simple, and can
easily be fooled by semicolons that do not terminate statements, like in
comments or strings.