# spark-docker

## install docker on docker

```bash
$ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
$ docker run -it -p 8088:8088 -p 8042:8042 -p 4040:4040 -h sandbox sequenceiq/spark:1.6.0 bash
$ sudo apt-get update
$ apt-cache policy docker-ce
$ sudo apt-get install -y docker-ce
$ sudo systemctl status docker

```

## install docker on centos

```bash
$ sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
$ sudo yum-config-manager \
    --add-repo \
    https://download.docker.com/linux/centos/docker-ce.repo
$ sudo yum-config-manager --enable docker-ce-edge
$ sudo yum-config-manager --enable docker-ce-testing
$ sudo yum-config-manager --disable docker-ce-edge
$ sudo yum makecache fast
$ sudo yum install docker-ce
$ yum list docker-ce.x86_64  --showduplicates | sort -r
$ sudo yum install docker-ce-<VERSION>
$ sudo systemctl start docker
$ sudo docker run hello-world

```
