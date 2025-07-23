FROM amazon/aws-lambda-dotnet:8-x86_64
#FROM amazonlinux:2

RUN dnf install openssl -y
RUN dnf install bash zip -y
RUN mkdir -p /tmp/layer

ENTRYPOINT ["sh", "-c", "cd /tmp/layer && mkdir -p bin && mkdir -p lib && cp /bin/openssl ./bin/openssl && cp /usr/lib64/libbz2.so.1 ./lib && cp /usr/lib64/libssl.so.3 ./lib && cp /usr/lib64/libcrypto.so.3 ./lib && zip -r layer.zip ./* && rm -rf lib bin"]

#ENTRYPOINT ["ls"]
