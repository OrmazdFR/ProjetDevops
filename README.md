# ProjetDevops
CI-CD project for ESGI


# Requirements 
Set `DOCKERHUB_TOKEN` and `DOCKERHUB_USERNAME` in the settings

(Repo settings > Security > Secrets and variables > Actions > New repository secret)

# Start project 
## Watchtower
docker run -e WATCHTOWER_POLL_INTERVAL=60 -d -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower devopspreprod devopsmain

## Preprod container
docker run --name devopspreprod -p 3000:3000 -d ormazd/devopspreprod

## Main container
docker run --name devopspreprod -p 3001:3000 -d ormazd/devopsmain