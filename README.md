# Install Docker Engine
http://docs.docker.com/engine/installation/

# Pull os161 image and run kernel
```bash
docker pull xcv58/os161
docker run --name os161 -w /root/ -t -i xcv58/os161
cd os161/root/
sys161 kernel
```

You may need `sudo` before `docker` command.

You should be able to boot os161.

Note that everytime you use `docker run` command, it actually runs two commands: `create` and `start`,
[more details](http://serverfault.com/questions/661909/the-right-way-to-keep-docker-container-started-when-it-used-for-periodic-tasks).

So next time you wanna access the same docker container, you need use

```
docker start -i os161
```

to connect the same container you created before.
