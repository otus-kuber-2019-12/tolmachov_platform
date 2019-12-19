FROM nginx:latest
RUN useradd -u 1001 appuser && \
    chown appuser /var/cache/nginx && \
    mkdir /app && \
    chmod 777 /app && \
    sed -i 's/^user .*//' /etc/nginx/nginx.conf && \
    sed -i 's#root .*#root /app;#g' /etc/nginx/conf.d/default.conf && \
    sed -i 's/listen .*/listen 8000;/g' /etc/nginx/conf.d/default.conf && \
    sed -i 's#/var/run/nginx.pid;#/tmp/nginx.pid;#g' /etc/nginx/nginx.conf
USER appuser
EXPOSE 8000
