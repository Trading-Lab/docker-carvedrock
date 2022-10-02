#Step 1
docker build -t dahlsailrunner2/carvedrockapi:latest -f .\CarvedRock.Api\Dockerfile .

#Step 2
docker images

#Step 3
docker run -p 5000:80 -e ASPNETCORE_ENVIRONMENT="Development" --name crtest -d carvedrockapi
