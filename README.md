# ssh-guide

## 代理
下面的命令，以 jump 作为跳板，将本地的 `6443` 端口转发到 `192.168.123.245`
```
ssh -L 0.0.0.0:6443:192.168.123.245:6443 jump
```

## Config
```
Host dev
  HostName 192.168.123.245
  User root
  ProxyJump jump

Host jump
  HostName 10.121.218.245
  User root
```
