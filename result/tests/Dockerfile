FROM node:22-bookworm
#Pour faire marcher en CI et en local
#FROM --platform=linux/amd64 node:22-bookworm

RUN apt-get update -qq && apt-get install -qy \ 
    ca-certificates \
    bzip2 \
    curl \
    libfontconfig \
    --no-install-recommends
RUN yarn global add phantomjs-prebuilt
ADD . /app
WORKDIR /app
CMD ["/app/tests.sh"]
