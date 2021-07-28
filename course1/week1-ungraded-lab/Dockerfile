ARG BASE_CONTAINER=jupyter/tensorflow-notebook:latest
FROM $BASE_CONTAINER
LABEL author="Binnur Al-Kazily"
USER root
WORKDIR /home/jovyan/work
# Copy requirements.tx to current directory
COPY ./requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt
COPY . .
# Switch back to jovyan to avoid accidental container runs as root
USER $NB_UID
