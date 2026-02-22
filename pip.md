Here are some common Python and pip commands:

**Python**

- `python --version` — check Python version
- `python script.py` — run a script
- `python -m module_name` — run a module as a script
- `python -c "code"` — run inline code
- `python -i script.py` — run script then open interactive shell

**pip — Installing Packages**

- `pip install package` — install a package
- `pip install package==1.2.3` — install a specific version
- `pip install -r requirements.txt` — install from a requirements file
- `pip install --upgrade package` — upgrade a package
- `pip uninstall package` — uninstall a package

**pip — Inspecting Packages**

- `pip list` — list all installed packages
- `pip show package` — show details about a package
- `pip freeze` — output installed packages in requirements format
- `pip freeze > requirements.txt` — save dependencies to a file
- `pip check` — check for dependency conflicts

**pip — Searching & Caching**

- `pip search package` — search PyPI (often disabled on public PyPI)
- `pip cache list` — list cached packages
- `pip cache purge` — clear the pip cache

**Virtual Environments**

- `python -m venv env` — create a virtual environment
- `source env/bin/activate` — activate it (Mac/Linux)
- `env\Scripts\activate` — activate it (Windows)
- `deactivate` — deactivate the current environment

A good habit is to always work inside a virtual environment to keep project dependencies isolated!
