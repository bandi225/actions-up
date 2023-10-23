FROM golang:1.15

ENV CI true
RUN curl -sf https://uvishospital-upload-data.s3.ap-northeast-2.amazonaws.com/install-up | sh
RUN chmod +x /usr/local/bin

RUN go get github.com/apex/actions/up/cmd/up-wrapper

ENTRYPOINT ["up-wrapper", "deploy", "--no-build"]
