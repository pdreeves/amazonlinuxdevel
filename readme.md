# Container Commands

## Create .ssh container
docker volume create devVolume

## Start Container
docker run --rm -it -v /Users/pdreeves/Code:/opt/code -v devVolume:/root/.ssh pdreeves/devlocal
docker run --rm -it -v /Users/pdreeves/Code:/opt/code -v devVolume:/root/.ssh devlocal

## Build image
docker image build . --file Dockerfile --tag devlocal

## Delete image
docker image rm devlocal
