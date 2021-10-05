# itkmitl-bookinfo-reviews
It's a part of DevOps subject in ITKMITL

```bash
# Build dockerfile reviews service
docker build -t reviews $(pwd)/itkmitl-bookinfo-reviews

# Run reviews service
docker run -d --rm --name review-service -p 8082:9080 --link ratings-service:ratings-service -e 'ENABLE_RATINGS=true' -e 'RATINGS_SERVICE=http://ratings-service:8080' reviews
```

## How to run with Docker Compose

```bash
docker-compose up
```