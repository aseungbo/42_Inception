#베이스가 될 이미지
FROM debian:buster 

#내가 원하는 대로 이미지 바꿈
RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install nginx -y
RUN apt-get install vim -y

# COPY    conf/default /
# RUN     mv default /etc/nginx/sites-available/default

# RUN     openssl genrsa -out server.key 4096 
# RUN     openssl req -new -key server.key -subj "/C=KR/ST=Seoul/O=42Seoul/OU=Shin" -out server.csr
# RUN     openssl req -x509 -in server.csr -key server.key -out server.crt
# RUN     mv server.crt /etc/ssl/certs/
# RUN     mv server.csr server.key /etc/ssl/private

# ENTRYPOINT     ["nginx", "-g", "daemon off;"]

#이미지에서 노출할 포트 -> 어차피 nginx는 default로 80번 포트를 open하지만 명시적으로 적어줌
EXPOSE 443