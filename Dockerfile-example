FROM debian:jessie
RUN apt-get update && apt-get install -y \
git \
vim
COPY abc.txt /src/abc.txt
CMD ["echo", "hello world"]
