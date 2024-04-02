## install docker

apt  install docker.io -y

docker -v

## clone github

git clone https://github.com/shaiksaiteja/finalproject.git

cd finalproject/

## build docker image
docker build -t newget .
## check image is created or not with newget
docker images

docker run <imgid> -p 8000:8000

## login to docker
docker login


## push img to dockerhub
docker tag <img-name> <dockerhub-username>/<dockerhub-repo-name>:tagname
docker push shaiksaiteja/finalsemproject:newget


ex:
docker tag newget shaiksaiteja/finalsemproject:newget
### newget : myimage name
### shaiksaiteja : dockerhub username
### finalsemproject : dockerhub repo name
### newget : tag giving to img 


# __________________________________________________________________________







docker pull shaiksaiteja/finalsemproject:newget

docker run -p 8000:8000 shaiksaiteja/finalsemproject:newget

