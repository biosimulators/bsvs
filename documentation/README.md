## Configuration for BioCompose Documentation.

### This documentation is created using ``sphinx``. To get started with sphinx, run the following commands:

1. Install sphinx into your environment with ``pip``:
    ```bash
    pip install sphinx sphinx-autodoc-typehints
    ```
2. Create a ``docs`` or ``documentation`` directory at the root of the ``bio-compose`` repo:
    ```bash 
    mkdir documentation && cd documentation
    ```
3. Run sphinx quickstart in documentation directory:
    ```bash
    sphinx-quickstart
    ```
4. Ensure auto-complete of documentation is possible from the package's docstrings in the autogenerated ``conf.py`` from #3:
    ```python 
    extensions = [
        'sphinx.ext.autodoc',
        'sphinx_autodoc_typehints',
        # other extensions that are preferred as per the sphinx documentation
    ]
    ```
5. Auto-generate documentation from the docstrings:
    ```bash 
    sphinx-apidoc -o /path/to/the/directory/with/index.rst /path/to/the/python/package/or/code/for/which/you/are/creating/the/documenation
    ```

6. Ensure you are in the directory in which the ``Makefile`` is stored and create the HTML. Be sure to read the returning message from this step:
    ```bash
    make html 
    ```
   

## Applying changes:

```bash
cd documentation && make clean && make html && cd ..
```