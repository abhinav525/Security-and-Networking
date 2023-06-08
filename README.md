
# Picoctf - babyshark two two two writeup

My first approach is to look at the arp protocol just to get an idea to what kind of  IPs are in the network:
 this was the result:
 
![arap.png]

the IP was: `192.168.38.104`

So when I searched for this IP particularly I got:
we got to know that this ip had only single packet sent soo this must be suspicious as it was a public IP directly being talked to:

![ip.png]

the ip was: `18.217.1.57`
now we had some lead.....

if we look at the dns traffic of this ip it lead to these many domains:
```
cGljb0NU.reddshrimpandherring.com
RntkbnNf.reddshrimpandherring.com
M3hmMWxf.reddshrimpandherring.com
ZnR3X2Rl.reddshrimpandherring.com
YWRiZWVm.reddshrimpandherring.com
fQ==.reddshrimpandherring.com

```

The subdomains of this ip combined will be your resultant base64 encoded string which will be our flag

cGljb0NURntkbnNfM3hmMWxfZnR3X2RlYWRiZWVmfQ==

decoded:
`picoCTF{dns_3xf1l_ftw_deadbeef}`
