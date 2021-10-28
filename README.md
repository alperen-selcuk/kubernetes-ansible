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

--add ssh key---

```
ssh-keygen -t rsa
