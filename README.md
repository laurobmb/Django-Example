# example-nginx


podman pod create --name django-pod -p8000:8000

podman run -d --pod django-pod --name django-app django:latest

podman run -d --name postgres-db --pod django-pod -v /tmp/postgresql:/var/lib/postgresql/data:Z -e POSTGRES_DB=postgres -e POSTGRES_USER=postgres -e POSTGRES_PASSWORD=postgres postgres:latest
