# Все оперции повторить для django и flask
1) В Dockerfile, убрать строки "улучшизмы"
```
FROM builder as dev-envs

RUN <<EOF
apk update
apk add git
EOF

RUN <<EOF
addgroup -S docker
adduser -S --shell /bin/bash --ingroup docker vscode
EOF
# install Docker tools (cli, buildx, compose)
COPY --from=gloursdocker/docker / /
```
2) Cобрать image руками ``docker build -t image_name .```
3) Запустить контейнер руками с помощью ```docker run -it -d --name container_name -p 8000:8000 image_name```, проверить что контейнер запустился и фреймворк внутри него работает. После успешных проверок погасить с помощью ```docker stop container_name``` и ```docker rm container_name```
4) Написать свой docker-compose.yml, с помощью которого запустить контейнер ```docker compose up -d```
