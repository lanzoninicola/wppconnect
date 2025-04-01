O Portainer web não permite bind de arquivos locais (nginx.conf)

**Solução**: crie uma imagem customizada com o nginx.conf embutido

# dockerfile

FROM nginx:latest
COPY nginx.conf /etc/nginx/nginx.conf

# bash to build the image and upload to the Docker Hub

docker build -t lanzoninicola/wppconnect-nginx:latest .
docker push lanzoninicola/wppconnect-nginx:latest

# public address

http://191.101.234.115:8081/
