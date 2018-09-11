FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    apache2 \
    && rm -rf /var/lib/apt/lists/*

COPY etc/apache2/ports.conf /etc/apache2/ports.conf
COPY etc/apache2/site-available/000-default.conf /etc/apache2/sites-available/000-default.conf

COPY html/ /var/www/html

EXPOSE 8080

CMD ["apachectl", "-D", "FOREGROUND"]

# dockerfile\Exercise2> docker build -t ubuntu:apache2 .
# dockerfile\Exercise2> docker run -it --rm -p 8080:8080 ubuntu:apache2