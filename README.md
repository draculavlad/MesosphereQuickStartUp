# MesosphereQuickStartUp
quick startup a simple 1-master-1-slave mesosphere cluster

## How Mesosphere Set Up##
Build script is coming from https://github.com/draculavlad/SetUpMesosphereOnCentos7WithServiceDiscovery.
Please execute these command with root priviledges!

## setup master##
```shell
wget https://raw.githubusercontent.com/draculavlad/SetUpMesosphereOnCentos7WithServiceDiscovery/master/mesos-master-setup.sh
chmod +x mesos-master-setup.sh
./mesos-master-setup.sh
```

### Things you need to know before you try to set up your slave node###
* let's just assume that your master ip address would be 192.168.1.1
```shell
wget https://raw.githubusercontent.com/draculavlad/SetUpMesosphereOnCentos7WithServiceDiscovery/master/mesos-slave-setup.sh
export master_node_ip="{your mesos master ip}"
sed -i "s|master_node_ip=|master_node_ip=$master_node_ip|g" mesos-slave-setup.sh
chmod +x mesos-slave-setup.sh
./mesos-slave-setup.sh
```
