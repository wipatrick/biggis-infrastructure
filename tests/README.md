## Prerequisite
Make changes to ```/etc/hosts```:
```
192.168.33.10   biggis.dev.net.node1
192.168.33.11   biggis.dev.net.node2
192.168.33.12   biggis.dev.net.node3
```
Make changes to ```~/.ssh/config``` by inserting the following entries and specifying the ```path/to``` IdentityFile:
```
Host biggis.dev.net.node1
    HostName 192.168.33.10
    Port 22
    StrictHostKeyChecking no
    UserKnownHostsFile /dev/null
    IdentitiesOnly yes
    User vagrant
    IdentityFile "path/to/biggis-infrastructure/tests/.vagrant/machines/node1/virtualbox/private_key"
    PasswordAuthentication no

Host biggis.dev.net.node2
    HostName 192.168.33.11
    Port 22
    StrictHostKeyChecking no
    UserKnownHostsFile /dev/null
    IdentitiesOnly yes
    User vagrant
    IdentityFile "path/to/biggis-infrastructure/tests/.vagrant/machines/node2/virtualbox/private_key"
    PasswordAuthentication no

Host biggis.dev.net.node3
    HostName 192.168.33.12
    Port 22
    StrictHostKeyChecking no
    UserKnownHostsFile /dev/null
    IdentitiesOnly yes
    User vagrant
    IdentityFile "path/to/biggis-infrastructure/tests/.vagrant/machines/node3/virtualbox/private_key"
    PasswordAuthentication no
```
