# docker-ossec
## OSSEC HIDS 2.9 Server Container
Forked from Atomicorp Official Docker Image

**FROM https://hub.docker.com/r/atomicorp/ossec-docker/  (forked for security of image sourcing)**

All credit goes to Atomicorp (and DanParriott et al).

**Launch:**
```docker run -d -p 1514:1514/udp -p 1515:1515/tcp --name ossec-server <image>```


**Launch with a specified Volume:**
```
docker volume create ossec-data
docker run -d -p 1514:1514/udp -p 1515:1515/tcp -v ossec-data:/var/ossec/data --name ossec-server atomicorp/ossec-docker
```


**Attach to running container:**
```docker exec -it ossec-server  bash```
