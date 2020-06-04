## Build project

```
cd lab3
vagrant up
vagrant ssh -c "ip a"
vagrant ssh
```

## Switch user to stack

```
sudo su - stack
cd devstack
./stack.sh
```

### Result success build

![success](./images/success.png)


## Flush iptables

```
sudo iptable -F
```

## open Browser http://192.168.50.10/dashboard

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
