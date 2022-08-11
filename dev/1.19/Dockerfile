FROM golang:1.19.0

RUN curl -sSfL https://raw.githubusercontent.com/cosmtrek/air/master/install.sh | sh -s \
    && mv ./bin/air /usr/bin/air

WORKDIR /var/www

ENTRYPOINT ["air"]
