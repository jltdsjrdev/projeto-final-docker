# Sistema de casa de eventos turma 1025

![Print da Homepage](https://i.ibb.co/0BLwdMW/Screenshot-2024-02-19-at-16-30-28.png)

## Tecnologias Utilizadas

- React
- Vite
- Node v20.5.1

## Dependências Utilizadas

- React Router
- Styled Components
- Axios
- React Toastify
- Json Server


## Instruções de Instalação

Clonar o projeto com o comando abaixo:

```sh
git clone https://github.com/jltdsjrdev/projeto-final-docker.git
```

Entrar na pasta do projeto

```sh
cd casa-de-eventos-react
```

Instalar as dependencias

```sh
npm install
```

## Instruções para rodar o projeto

Digitar o comando para criar a imagem do docker baseado nos requisitos do Dockerfile

```sh
docker buildx buld -t casa-de-eventos-react .
```
Digitar o comando para rodar a imagem do docker em uma porta especifica


```sh
docker run -d -p 5173:5173 casa-de-eventos-react
```

### Pronto! Seu projeto já estará rodando no endereço

```sh
http://localhost:5173
```
Caso haja necessidade de mudanças no código

```sh
docker ps
```
Olhe o id do container

```sh
CONTAINER ID   IMAGE                   COMMAND                  CREATED          STATUS          PORTS                                       NAMES
fb9d05203a74   casa-de-eventos-react   "docker-entrypoint.s…"   31 minutes ago   Up 31 minutes   0.0.0.0:5173->5173/tcp, :::5173->5173/tcp   nervous_jennings
```

Pare o container

```sh
docker stop <id do container>
```

Faça suas mudanças e rode novamente os comandos de "build e "run".

### Para rodar e ver o json no backend

```sh
http://localhost:5173/events.json
```

![imagem projeto](https://github.com/user-attachments/assets/afa94a7c-acb7-42fe-a14f-897bb8d16e19)


### Guardar imagem Docker no Docker Hub

```sh
docker login
```
Depois

```sh
docker tag <tag do nome da imagem> <tag do usuario do docker hub>/<tag do nome da imagem>:<tag da versão>
Exemplo: docker tag casa-de-eventos-react vapeprosper/casa-de-eventos-react:v.1
```

Publicar no Docker Hub

```sh
docker push <tag do usuario do docker hub>/<tag do nome da imagem>:<tag da versão>
docker push vapeprosper/casa-de-eventos-react:v.1
```

### Imagem no docker Hub

https://hub.docker.com/r/vapeprosper/casa-de-eventos-react

### Agradecimentos

Codigos de React, Vite, Node e estruturação completa: https://github.com/roofranklin
