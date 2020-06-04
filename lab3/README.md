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
vagrant snapshot save devstack3 lab3
```


```
vagrant snapshot restore lab3 
```

### Referece Using save:

```
vagrant snapshot save [vm-name] NAME
```

Saves a new snapshot with the names of your VM and your snapshot.

Using restore:

```
vagrant snapshot restore [vm-name] NAME
```

Restores the named snapshot.

Options:

```
--[no-]provision – forces the provisioners to run (or prevent them from doing so).
```