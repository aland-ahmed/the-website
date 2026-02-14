FROM nginx:alpine

LABEL maintainer="azad.hama123@gmail.com"
LABEL version="1.0.0"
LABEL description="GitOps Learning Website"

COPY index.html /usr/share/nginx/html/index.html
COPY style.css /usr/share/nginx/html/style.css

COPY nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 8080

HEALTHCHECK --interval=30s --timeout=3s --start-period=5s --retries=3 CMD wget --quiet --tries=1 --spider http://localhost:8080/ || exit 1

CMD ["nginx", "-g", "daemon off;"]