<!-- TITLE: Rancher -->
<!-- SUBTITLE: A quick summary of Rancher -->

# Create Hosts

```sh
docker-machine create -d virtualbox --virtualbox-boot2docker-url https://releases.rancher.com/os/latest/rancheros.iso rancher01

eval $(docker-machine env rancher01)

docker run --rm --privileged -v /var/run/docker.sock:/var/run/docker.sock -v /var/lib/rancher:/var/lib/rancher rancher/agent:v1.2.6 http://172.29.14.182:8080/v1/scripts/CB13326EC1C5D90C5C7D:1483142400000:fZHAfJSltMfSNwnmdyaNtCNvkU

eval $(docker-machine env -u)
```

