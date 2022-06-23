# ssh远程

## 远程方式

```
ssh username@ip
```

## 不需要密码连接

<font color='red'>检查~/.ssh目录是否存在</font>

mac上

```
cat ~/.ssh/id_rsa.pub | ssh user@ip "cat >>  ~/.ssh/authorized_keys"
```

服务器上

```shell
vim /etc/ssh/sshd_config
# 修改下面的yes为no
PubkeyAuthentication no
```

## “Warning: Remote Host Identification Has Changed” Error

```
vim ~/.ssh/known_hosts
# 将带服务器ip的那一行输出
```

