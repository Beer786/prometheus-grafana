FROM golang:1.16-alpine
WORKDIR /app

COPY . ./
RUN go mod download
RUN go build -o /simpleweapp
EXPOSE 8000
CMD [ "/simpleweapp" ]
