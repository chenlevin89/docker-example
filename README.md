# Build
docker build -f Dockerfile.v1 -t docker-example-v1 .


# Run
docker run -p 4200:4200 -d docker-example-v1


# Multi platform 

docker buildx build -f Dockerfile.v5 \\
 --platform linux/amd64,linux/arm64 -t chenlevin/docker-example-v5:multi --push .


docker buildx imagetools inspect chenlevin/docker-example-v5:multi
# docker-example
