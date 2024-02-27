# FastAPI Initializer at VSCode

1. create .venv
    ```
    pwd 
    $ `your-device-path`/fastapi-init-vscode
    mkdir .venv
    ls -a | grep .venv
    $ .venv

    ```
1. let's install module by poetry 
    ```
    poetry install
    ```

## Appendix
if you settings python version in poetry, you setting this.
1. If you already created `.venv`, you must remove `.venv`
    ```
    $ python -m venv .venv
    ```
1. Edit your pyproject.toml
    ```
    $ grep -a2 python pyproject.toml
    [tool.poetry.dependencies]
    python = "^3.10"
    fastapi = "^0.79.0"
    uvicorn = {extras = ["standard"], version = "^0.18.2"}
    ```

    ```
    python = "^3.10" -> "^3.10.7"
    ```
    
    ```
    $ grep -a2 python pyproject.toml
    [tool.poetry.dependencies]
    python = "^3.10.7"
    fastapi = "^0.79.0"
    uvicorn = {extras = ["standard"], version = "^0.18.2"}
    ```

1. Set python version.
    ```
    $ poetry env use 3.10.7
    ```
    ※If you don't have python other version, you must install the one.
    ※If you want to use `python3.10`, you must set `pyenv`.

1. Set modules.
    ```
    poetry add fastapi uvicorn[standard]
    ```
    or 
    ```
    poetry update && poetry install
    ```

1. Change setting.json python version path.
    
    You should change python path of setting.json.
