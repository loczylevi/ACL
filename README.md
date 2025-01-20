# ACL

```bash
access-list 1 deny 192.168.2.0 0.0.0.255
access-list 1 permit any
int g0/0
ip acess-group 1 out
```
