FROM caddy:2.10.0 AS builder
RUN xcaddy build \
  --with github.com/caddy-dns/duckdns

FROM caddy:2.10.0
COPY --from=builder /usr/bin/caddy /usr/bin/caddy
