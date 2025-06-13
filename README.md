Descrição Geral

Este projeto tem como objetivo ensinar na prática os conceitos de CI/CD utilizando as tecnologias FastAPI, Docker, Jenkins e Kubernetes. Os bolsistas trabalharão com um código base em FastAPI e desenvolverão uma esteira de automação que fará o deploy automatizado da aplicação em um cluster Kubernetes local.


Tecnologias Utilizadas

· Github: Versionamento de códigos.

· FastAPI: Framework web em Python.

· Docker: Para conteinerização da aplicação.

· Docker Hub: Registro público de imagens.

· Jenkins: Ferramenta de CI/CD.

· Kubernetes local: Minikube, Kind, Docker Desktop ou Rancher Desktop.

Código Base da Aplicação (Backend) projeto-kubernetes-pb-desafio-jenkins/backend/main.py at main · box-genius/projeto-kubernetes-pb-desafio-jenkins · GitHub


Fases do Projeto

Fase 1: Preparação do projeto

Nesta fase será necessário crias as seguintes atividades:

· Criar um repositório de código no Github para inserir a aplicação de exemplo;
-- como este repositorio por exemplo
· Criar conta no Docker Hub.
-- https://hub.docker.com/
· Verificar acesso ao cluster Kubernetes local.
-- para este projeto estou usando rancher desktop
· Validar execução local com uvicorn.
teste local com uvicorn
![Captura de Tela (71)](https://github.com/user-attachments/assets/03ec83d6-5479-4729-b45e-595664cf92df)

Feito: Código rodando localmente, repositório do github criado e ambiente preparado.

Fase 2: Conteinerização com Docker

Nesta fase é esperado que se execute o backend, incrementando esses códigos em containers e depois faça a publicação deste container no Dockerhub

· Para teste local e ver se está funcionando, pode criar docker-compose (opcional);

· Fazer build: docker build -t usuario/fastapi-hello:latest .

· Fazer push: docker push usuario/fastapi-hello:latest

· Versionar o dockerfile junto com o código da aplicação no github.


Entregáveis: Imagem publicada no Docker Hub.
