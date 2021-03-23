
### Gerar o build do docker ###
./mvnw.cmd package && java -jar target/validarCpf.jar

### Gerar o build do docker ###
docker build -t eduardotech/validador-cpf-csharp -f Dockerfile .

### Rodar imagem docker e gravar localmente ###
docker run -d -p 5001:80 --name validador-cpf-csharp eduardotech/validador-cpf-csharp

### Rodar imagem docker em modo iterativo localmente ###
docker run -it -p 5001:80 --name validador-cpf-csharp eduardotech/validador-cpf-csharp

### para parar o serviço###
docker stop validador-cpf-csharp

### para startar o serviço ###
docker start validador-cpf-csharp

### para remover o serviço ###
docker rm validador-cpf-csharp

### Para se logar no dockerhub ###
docker login

### Criar a tag apontando para o repositorio do docker hub ###
docker tag eduardotech/validador-cpf-csharp + URL Docker

### Fazer push da imagem para o docker hub ###
docker push eduardotech/validador-cpf-csharp
