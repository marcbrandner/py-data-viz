FROM jupyter/datascience-notebook:latest

COPY --chown=${NB_UID}:${NB_GID} requirements.txt /tmp/

RUN pip install --no-cache-dir --requirement /tmp/requirements.txt && \
    fix-permissions "${CONDA_DIR}" && \
    fix-permissions "/home/${NB_USER}"

#RUN jupyter labextension install jupyterlab-plotly --no-build && \
#    jupyter lab build --minimize=False