FROM alpine:3.10
ARG uid
ARG gid
ARG user
ARG group

RUN apk add --no-cache nodejs npm
RUN npm i -g ionic

EXPOSE 8100

RUN addgroup -g $gid $group && adduser -D -G $group -u $uid $user
USER $user

VOLUME ["/code"]
WORKDIR /code

CMD ["ionic", "serve", "--address=0.0.0.0"]
