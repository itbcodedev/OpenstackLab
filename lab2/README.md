## Single node  Devstack

install devstack  on single interface

```
cd lab2
vagrant up

vagrant ssh
sudo su - stack

./stack.sh
```

### Success result



### Flush iptables

```
sudo iptables -F
```

## open Browser http://127.0.0.1:8080/dashboard


![success](./images/login.png)

## Use vagrant to manage snapshot

- Exit to host machine

```
vagrant snapshot save  lab3
```


```
vagrant snapshot restore lab3 
```

### Referece Using save:

- List Snapshots

```
vagrant snapshot list
```

- Create a Snapshot

```
vagrant snapshot save SNAPSHOTNAME
```

```
vagrant snapshot save snapshot01
```

- Restore a Snapshot

```
vagrant snapshot restore SNAPSHOTNAME
```

```
vagrant snapshot restore snapshot01
```

- Delete a Snapshot

```
vagrant snapshot delete SNAPSHOTNAME
```

