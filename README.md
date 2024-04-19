# Ping

Aplicação Java com container para exemplo

## Pré-requisitos

- Java 17+
- Docker 
- Acesso a internet
- Acesso ao Docker Hub

## Instalação

#### Clone

```
https://github.com/TiagoAlcan/checkpoint2.git
```

## Execução


#### Docker

* Criar imagem

```
docker build -t checkpoint2 .
```

* Executar container

spring.profiles.active=<prd|dev|stg>

```
docker run -d -p 8080:8080 -e PROFILE=<prd|dev|stg> checkpoint2
```

## Container Registry


#### Docker Hub

* Login

```
docker login -u <username>
```

* Criar imagem pronta para upload (método 1 - criando nova imagem)


```
docker build -t <username>/checkpoint2 .
```


* Criar imagem pronta para upload (método 2 - renomeando imagem existente)


```
docker tag checkpoint2 tiagoalcan/checkpoint2
```


* Upload de imagem para o Docker Hub


```
docker push tiagoalcan/checkpoint2 
```

*Comando docker para executar a aplicação a partir do docker hub com o profile "dev" (desenvolvimento) - H2

```
docker run -d -p 8080:8080 -e PROFILE=dev tiagoalcan/checkpoint2
```

*Comando docker para executar a aplicação a partir do docker hub com o profile "prd" (produção) - Oracle SQL developer

```
docker run -d -p 8080:8080 -e PROFILE=prd tiagoalcan/checkpoint2 
```

*Comando docker para executar a aplicação a partir do docker hub com o profile "stg"(stagging - homologação) - MySQL

```
docker run -d -p 8080:8080 -e PROFILE=stg tiagoalcan/checkpoint2 
```

#### Navegação

- Base

http://localhost:8080


## Features (Funcionalidades)

- Múltiplos profiles

## Contatos

- Tiago Gomes Alcântara - tiago.gomesalcan@email.com
- Guilherme Loureiro - guilhermelsba@email.com

## Referencias

Meu GitHub: - [GitHub](https://github.com/TiagoAlcan)

Meu DockerHub: - [DockerHub](https://hub.docker.com/u/tiagoalcan)
