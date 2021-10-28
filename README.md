# kubernetes-ansible

##this project uses to provision kubernetes cluster with ansible.

first you can create ansible admin user both nodes and ansible server.

---add user---

```
useradd -m -d /home/ansible ansible
passwd ansible
```

---add sudoers ansible user---

```
ansible ALL=NOPASSWD:   ALL
```

change all nodes /etc/ssh/sshd_config "PasswordAuthentication yes" config and "systemctl restart sshd"

PasswordAuthentication yes


--add ssh key nodes---

```
ssh-keygen -t rsa
ssh-copy-id -i ~/.ssh/id_rsa.pub master
ssh-copy-id -i ~/.ssh/id_rsa.pub worker1
ssh-copy-id -i ~/.ssh/id_rsa.pub worker2
```

now you can reach all host and work with ansible.
