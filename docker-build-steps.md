# Carved Rock - Docker (Build PS: Steps)

## Step 1
docker build -t carvedrockapi2:latest -f .\CarvedRock.Api\Dockerfile .
docker images

## Step 2
docker run -p 5000:80 -e ASPNETCORE_ENVIRONMENT="Development" --name crtest -d carvedrockapi2

docker container ls -a
docker rm 3c0

docker image rm 61995a2a0327


## Tag & Push
docker tag carvedrockapi2:latest samuelmano/mycarvedrockapi
docker push samuelmano/mycarvedrockapi

## From Docker Hub
docker pull samuelmano/mycarvedrockapi
