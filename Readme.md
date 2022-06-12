# Python Application Dockerised

## ⚠️ I don't own this script

This script is taken from python-engineer's movie picker just for learning to dockerise the application

Link : https://github.com/python-engineer/python-fun/blob/master/moviepicker/main.py

## Dockerising

First we need to make our dockerfile in order to dockerise it

```Dockerfile
# Dockerfile, Image, Container

FROM python:3.8

ADD main.py .

RUN pip install requests beautifulsoup4

CMD ["python", "./main.py"]
```

Now we will create an image out of it :

Open your terminal

```bash
docker build -t python-movie-imdb .
```

Check if your image is build using

```bash
docker images

# OUTPUT

REPOSITORY          TAG       IMAGE ID       CREATED          SIZE
python-movie-imdb   latest    80eca***2e87   25 seconds ago   923MB
debian              latest    4ea***30377a   2 weeks ago      124MB
hello-world         latest    feb5d9****a5   8 months ago     13.3kB
```

Run you image in a container

```bash
docker run -it python-movie-imdb
```
