
# Image1
FROM golang
ADD main.go /root
WORKDIR /root
RUN go build -o /root/mainApp /root/main.go


# Image2 - alpine(ubuntu나 centos보다 가벼움)
FROM alpine:latest
WORKDIR /root

# --from=0 첫번째에서 빌드된 최종 Image에서 실행 파일만 복사
COPY --from=0 /root/mainApp .
CMD ["./mainApp"]