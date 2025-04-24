FROM nginx:stable

COPY certs /etc/nginx/certs
COPY templates/default.conf.template /etc/nginx/templates/default.conf.template

CMD ["sh", "-c", "envsubst '\\$CERT_FILE \\$KEY_FILE \\$GATEWAY_PORT' < /etc/nginx/templates/default.conf.template > /etc/nginx/conf.d/default.conf && nginx -g 'daemon off;'"]
