FROM ubuntu:17.04

RUN apt-get update && \
    apt-get install --yes --no-install-recommends \
    percona-toolkit

CMD pt-kill \
    --busy-time "${MAX_QUERY_TIME}" \
    --interval 60 \
    --user "${MYSQL_USERNAME}" \
    --password "${MYSQL_PASSWORD}" \
    --host "${MYSQL_HOST}" \
    --kill \
    --print
