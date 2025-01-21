# ACL

```bash
access-list 1 deny 192.168.2.0 0.0.0.255
access-list 1 permit any
int g0/0
ip acess-group 1 out
```


```bash

ip access-list extended SURFING
Remark permit inside HTTP and HTPS traffic
 permit tcp 192.168.1.0 0.0.0.127 any eq 443
 permit tcp 192.168.1.0 0.0.0.127 any eq 80
exit
ip access-list extended BROWSING
Remark only permit returnin htp and htps traffc
 permit tcp any 192.168.1.0 0.0.0.255 established
exit

int g0/0
ip access-group SURFING in
ip access-group BROWSING out
end
sh acces-list
```
