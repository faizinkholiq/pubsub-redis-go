# golang
FROM golang:1.17.3-buster

# working dir
WORKDIR /app

COPY . .

# auto build & run
RUN go get github.com/githubnemo/CompileDaemon
RUN go mod vendor
ENTRYPOINT CompileDaemon --build="go build -o /go/bin ./main.go" --command="/go/bin/main"