FROM golang:alpine as builder

WORKDIR /go/src/app

COPY . .

RUN CGO_ENABLED=0 go build -o /msg main.go

FROM scratch

COPY --from=builder /msg /msg

CMD ["/msg"]


