# Container/Contêiner
Docker and Kubernetes


### Dockerfile

```
FROM ubuntu
RUN echo "hello there"
```

Para criar imagem do Dockerfile:
`docker build --tag 'image-name' .`

Para executar imagem criada com --attach (STDIN | STDOUT | STDERR), permitindo anexar o terminal à saída do container em tempo real:  
`docker run --attach (or -a) stdout --name 'container-name' 'image-name'`  
`docker run -a stdout --name 'container-name' 'image-name'`

Para executar imagem criada com --detach, permitindo a execução do container em segundo plano:  
`docker run --detach (or -d) --name 'container-name' 'image-name'`

Para executar imagem criada com --interactive e --tty, mantendo a entrada do terminal aberta durante a execução do contêiner:  
`docker run --interactive (or -i) --tty (or -t) --name 'container-name' 'image-name'`  
`docker run -it 'image-name' /bin/bash`  
`docker run -it 'image-name' /bin/bash -c "echo 'Hello, Docker!'"`  
`docker run -id 'image-name'`  

