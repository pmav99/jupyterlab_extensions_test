# JEODPP + jupyterlab + extensions

## Extension list

We currently use the following jupyterlab extensions:

- `jupyter-widgets/jupyterlab-manager`
- `jupyter-widgets/jupyterlab-sidecar`
- `bokeh`
- `bqplot`
- `ipycanvas`
- `ipyevents`
- `ipytree`
- `jupyter-leaflet`
- `jupyter-matplotlib`
- `qgrid2`

In order to install these we need to install both python packages and the corresponding jupyterlab extensions

## Install Python dependencies

First, create a venv and install the dependencies from `pyproject.toml` with poetry:

``` bash
python3 -mvenv venv
source venv/bin/activate
poetry install
```

## Install jupyterlab extensions

Run (and wait):

```
jupyter labextension install --no-build @jupyter-widgets/jupyterlab-manager@2.0.0
jupyter labextension install --no-build @jupyter-widgets/jupyterlab-sidecar@0.5.0
jupyter labextension install --no-build @bokeh/jupyter_bokeh@2.0.4
jupyter labextension install --no-build bqplot@0.5.19
jupyter labextension install --no-build ipycanvas@0.6.1
jupyter labextension install --no-build ipyevents@1.8.1
jupyter labextension install --no-build ipytree@0.1.8
jupyter labextension install --no-build jupyter-leaflet@0.13.2
jupyter labextension install --no-build jupyter-matplotlib@0.7.4
jupyter labextension install --no-build qgrid2@1.1.3
jupyter lab build
```

## Test

Run `jupyter lab` and open the notebook
