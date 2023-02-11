# datascience-notebook

docker-compose.yml

```
version: '3'
services:
  notebook:
    image: jupyter/datascience-notebook
    ports:
      - '8888:8888'
    environment:
      - JUPYTER_ENABLE_LAB=yes
      - TZ=Asia/Tokyo
    volumes:
      - ./work:/home/jovyan/work
    working_dir: /home/jovyan/work
    command: start-notebook.sh --NotebookApp.token=''
```
