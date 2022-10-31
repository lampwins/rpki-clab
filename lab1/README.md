# Simple BGP lab using FRR

This is a simple BGP lab consisting of 3 routers and 2 hosts. Each router belongs to a unique AS and the goal is to achive reachability between the two hosts, by routing through all three routers.

## Running the lab

Start the lab

```bash
$ containerlab deploy --topo frr01.clab.yml
```

Configure the host interfaces

```bash
$ ./host-interfaces.sh
```

Attempt a ping from host 1 to host 2

```bash
$ docker exec -it clab-frr01-h1 ping -c 4 192.168.13.2
```
