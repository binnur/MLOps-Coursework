ARG BASE_CONTAINER=jupyter/tensorflow-notebook
FROM $BASE_CONTAINER
LABEL author="Binnur Al-Kazily"
USER root
RUN pip install cvlib opencv-python-headless Pillow uvicorn python-multipart fastapi nest-asyncio
# Switch back to jovyan to avoid accidental container runs as root
USER $NB_UID
