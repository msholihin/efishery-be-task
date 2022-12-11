FROM golang:1.17

WORKDIR /usr/src/app

COPY ./go-auth-app ./app
COPY ./cache ./cache
COPY ./.jwt_pass ./.jwt_pass

RUN ls -al
RUN cd ./app && go mod download && go mod verify
RUN cd ./app && go build main.go

EXPOSE 9000/tcp

WORKDIR ./app

CMD ["./main"]
