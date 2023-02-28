FROM nginx:latest

# Copiar o arquivo de configuração personalizado do Nginx
COPY sites-available /etc/nginx/sites-available
COPY nginx.conf /etc/nginx/nginx.conf

# Copiar arquivos estáticos para o diretório padrão do Nginx
#COPY html /usr/share/nginx/html

RUN mkdir /etc/nginx/sites-enabled
RUN ln -s /etc/nginx/sites-available/*.conf /etc/nginx/sites-enabled/


# Expor a porta 80 do container
EXPOSE 80

# Iniciar o servidor Nginx
CMD ["nginx", "-g", "daemon off;"]
