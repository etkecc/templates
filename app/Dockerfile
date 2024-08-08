FROM ghcr.io/etkecc/base/build AS builder

WORKDIR /app
COPY . .
RUN just build

FROM ghcr.io/etkecc/base/app

ENV PROJECT_DB_DSN /data/PROJECT.db

COPY --from=builder /app/PROJECT /bin/PROJECT

USER app

ENTRYPOINT ["/bin/PROJECT"]

