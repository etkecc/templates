FROM ghcr.io/etkecc/base/build AS builder

WORKDIR /app
COPY . .
RUN just build

FROM scratch

ENV PROJECT_DB_DSN /data/PROJECT.db

COPY --from=builder /etc/ssl/certs/ca-certificates.crt /etc/ssl/certs/
COPY --from=builder /app/PROJECT /bin/PROJECT

USER app

ENTRYPOINT ["/bin/PROJECT"]

