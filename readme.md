# Comandos básicos Docker
# Imagens Docker
Procurar imagem no [Docker Hub](https://hub.docker.com/) e baixar
```
docker pull {nome da imagem}
```
## Listar imagens
```
docker image ls
```

## Apagar imagem
```
docker rmi {nome da imagem}
```

# Container
Criar container

Exemplo: Postgres
```
docker run --name {nome do container} -e POSTGREES_ROOT=root -e POSTGRESS_PASSWORD=root -p 5432:5432 -d postgres
```
-e: Variavel de ambiente

-p: Porta

-d: Para rodar em background

## Listar container rodando
```
docker ps
```

## Listar container na máquina
```
docker ps -a
```

## Iniciar container
```
docker start {nome do container}
```

## Parar container
```
docker stop {nome do container ou container id}
```

## Apagar container 
```
docker rm {nome do container}
```

# Preparar Banco de Dados
## Acessar container
```
docker exec -it {nome do container} bash
```
## Logar no Postgres
```
psql -U {nome do usuario}
```

## Listar bases de dados no postgres
```
\l
```

## Conectar na base de dados
```
\c {nome da base}
```

## Listar tabelas
```
\dt
```

