FROM kong:2.8.1
COPY ./kong.yml /kong/temp.yml
USER 0
RUN apk update && apk add gettext
USER kong
ENTRYPOINT bash -c 'envsubst < /kong/temp.yml > /kong/kong.yml && /docker-entrypoint.sh kong docker-start'
