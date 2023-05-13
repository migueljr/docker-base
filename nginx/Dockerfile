FROM nginx:latest

# Copiar o arquivo de configuração personalizado do Nginx
COPY sites-available /etc/nginx/sites-available
COPY nginx.conf /etc/nginx/nginx.conf
COPY default.conf /etc/nginx/conf.d/default.conf

COPY localhost.crt /etc/nginx/certs/localhost.crt
COPY localhost.key /etc/nginx/certs/localhost.key

# Copiar arquivos estáticos para o diretório padrão do Nginx
#COPY html /usr/share/nginx/html

RUN mkdir /etc/nginx/sites-enabled
RUN ln -s /etc/nginx/sites-available/*.conf /etc/nginx/sites-enabled/


# Expor a porta 80 do container
EXPOSE 80
EXPOSE 443

# Iniciar o servidor Nginx
CMD ["nginx", "-g", "daemon off;"]
