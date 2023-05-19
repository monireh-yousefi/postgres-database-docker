FROM alpine

RUN apk --update add postgresql-client
RUN mkdir /app
COPY ./app /app

ENV POSTGRES_HOST=localhost
ENV POSTGRES_PORT=5555
ENV POSTGRES_DB=mahdi_db
ENV POSTGRES_USER=mahdi
ENV POSTGRES_PASSEORD=password

ENTRYPOINT psql -a -f /app/query.sql postgresql://${POSTGRES_USER}:${POSTGRES_PASSEORD}@${POSTGRES_HOST}:${POSTGRES_PORT}/${POSTGRES_DB}
