FROM caddy:2-builder-alpine AS caddy_builder

RUN xcaddy build \
	--with github.com/dunglas/mercure/caddy \
	--with github.com/dunglas/vulcain/caddy

# Caddy image
FROM caddy:2-alpine AS caddy

COPY --from=caddy_builder --link /usr/bin/caddy /usr/bin/caddy
COPY --link Caddyfile /etc/caddy/Caddyfile