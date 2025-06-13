Descrição Geral

Este projeto tem como objetivo ensinar na prática os conceitos de CI/CD utilizando as tecnologias FastAPI, Docker, Jenkins e Kubernetes. Os bolsistas trabalharão com um código base em FastAPI e desenvolverão uma esteira de automação que fará o deploy automatizado da aplicação em um cluster Kubernetes local.


Tecnologias Utilizadas

· Github: Versionamento de códigos.

· FastAPI: Framework web em Python.

· Docker: Para conteinerização da aplicação.

· Docker Hub: Registro público de imagens.

· Jenkins: Ferramenta de CI/CD.

· Kubernetes local: Rancher Desktop.

Código Base da Aplicação (Backend) projeto-kubernetes-pb-desafio-jenkins/backend/main.py at main · box-genius/projeto-kubernetes-pb-desafio-jenkins · GitHub


Fases do Projeto

Fase 1: Preparação do projeto

Nesta fase será necessário crias as seguintes atividades:

· Criar um repositório de código no Github para inserir a aplicação de exemplo;
-- como este repositorio por exemplo
· Criar conta no Docker Hub.
-- https://hub.docker.com/

· Verificar acesso ao cluster Kubernetes local.

· Validar execução local com uvicorn.

teste local com uvicorn

![Captura de Tela (71)](https://github.com/user-attachments/assets/03ec83d6-5479-4729-b45e-595664cf92df)

Feito: Código rodando localmente, repositório do github criado e ambiente preparado.

Fase 2: Conteinerização com Docker

Nesta fase é esperado que se execute o backend e frontend, incrementando esses códigos em containers e depois faça a publicação deste container no Dockerhub
front
· Para teste local e ver se está funcionando, pode criar docker-compose (opcional);

· Fazer build: docker build -t usuario/meu-frontend:v1.0.0

· Fazer push: docker push usuariomeu-frontend:v1.0.0

· Para teste local e ver se está funcionando, pode criar docker-compose (opcional);
back
· Fazer build: docker build -t usuario/meu-backend:v1.0.0

· Fazer push: docker push usuario/meu-backend:v1.0.0

· Versionar o dockerfile junto com o código da aplicação no github.

![Captura de Tela (77)](https://github.com/user-attachments/assets/a2f9e7df-0eda-4031-85c9-e64cb72118fe)


Fase 3: Arquivos de Deploy no Kubernetes

Nesta fase vamos manualmente criar o deployment e service do kubernetes para que rode a imagem de container que acabamos de subir na fase anterior, no Kubernetes local.

· Criar o yaml de deployment da aplicação e aplicá-lo no cluster

· Criar o yaml de service do deploymento e aplicá-lo no cluster


Entregáveis: Aplicativo exposto em localhost:30001 via NodePort ou rodando via port-forward. O aplicativo precisa estar funcionando a partir do Kubernetes.

![Captura de Tela (75)](https://github.com/user-attachments/assets/defeed5e-0551-416a-9c67-de15937a2004)
![Captura de Tela (76)](https://github.com/user-attachments/assets/fff39fae-7c67-4b98-be09-b44f274e4611)


Fase 4: Jenkins - Build e Push


Nesta fase vamos criar uma pipeline no jenkins que quando acionada, seja manualmente ou por alguma mudança no repositório do github, execute o build e o push da imagem de container.

· Criar a pipeline no Jenkins;

· Realizar o stage de build;

· Realizar o stage de push;

· Fazer assim que commitar com o git push acionar automatico a pipeline no jenkins

Entregáveis: Pipeline funcional no Jenkins até o push da imagem.


Fase 5: Jenkins - Deploy no Kubernetes

Nesta fase o Jenkins será configurado para acessar o kubectl e acesso ao cluster local, assim como uma etapa de deploy será incluída no pipeline.

· Jenkins precisa acessar o kubectl (usar agent com kubectl e kubeconfig configurados);

· Adicionar etapa de deploy no Jenkinsfile;

· Testar a pipeline completa;

Entregáveis: Pipeline completo com deploy automatizado.
