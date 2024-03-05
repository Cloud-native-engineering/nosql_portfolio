# ETCD - Key-Value-Store

Etcd is a distributed key-value store that serves as a highly reliable data store. Developed by CoreOS, it is written in Go and is part of the Cloud Native Computing Foundation (CNCF). Etcd is commonly used as a distributed configuration store and a coordination service for distributed systems such as Kubernetes, providing a consistent and highly available way to store and retrieve data across a cluster of machines. Its simple HTTP API and strong consistency model make it a popular choice for building resilient distributed applications.

## Interacting with etcd

To interact with etcd the 'etcdctl' can be used. Followed the simpliest operation are documented:

### Write

```bash
etcdctl put <key> <value>
```

### Read

```bash
etcdctl get <key>
```

### Delete

```bash
etcdctl del <key>
```

### Add User

```bash
etcdctl user add <user>:<password>
````

### Enforce Authentication

```bash
etcdctl user add root:<password>

etcdctl auth enable
```

## Installation

The installation Process was documented in the following cloud-init-script with ansible tasks:

- [Install etcd with Cloud-Init and Ansible](https://github.com/Cloud-native-engineering/ansible_pull/blob/main/cloud_init/etcd.yml)
`