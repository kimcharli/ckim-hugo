---
title: "Certificate Authority"
date: 2018-11-10T02:50:14-05:00
draft: false
---

Under Construction

## create private key

```
ckim-mbp:temp ckim$ openssl genrsa -out myserver.com.key.pem 2048      
Generating RSA private key, 2048 bit long modulus
.......................................................................................................................................+++
................................................................................+++
e is 65537 (0x10001)
ckim-mbp:temp ckim$
ckim-mbp:temp ckim$ cat myserver.com.key.pem
-----BEGIN RSA PRIVATE KEY-----
MIIEowIBAAKCAQEAsl995BSNc6aflms0F+cyYW+Eja+KtdaSvuavzO019GkaR/J9
AH04TrMp4Y4dMQa051WYwVbK2Hyh5VBa5Sk1+xrG6WExpu10ZlrSrTVcMlYnOFDP
ejRsBQYbQpiLxIKa4uhzI0FH2xtOOTfSc35iBO2H2nj5EZUUA6r/jdB5C0JujaEo
UaMsHny8MyXdwRgYcLVrZEGocs7ch9Zvqk6wBZnE7DbKqLkqMY2gCoK7ZgIyxX6v
bpEn/Gjvb+VspnEPwWLRKrAvuYyAfPxhtwR/Gg1UJu1m3n3V7GWtFiF5FaY/CVkW
SIV9TNk9BmhcTc2EDwxb3wEOuPrlo2rHgkeE6QIDAQABAoIBADowAn5b4gT/LwI/
uH+vsPSuD1y1Dhfhhn91+5VrMHWpr6QWy4ZUUwEBW0E0PfuXR35Lowg3CvbyOVH4
E568AdsHUiohxbPBtH4LVLyiMpBNIIAzhGtGHJLK+iuQXc/eFy68S4sNqaYlUzBB
MIryiIE5B19SpVWB/0RvDOyzPDlah6rEBW1CzV26JqA+9BixEc1ThwVMxlV8oNVV
lWdaRXHpgRDcRucead1kBG1nhRy7gECTYhRaI9bw1wJ9M1xEFFoSjkXeWvM+DDMq
MxkO3e9BnBN+91h87jXPjUBmfQt3tGMQuthrG5Fhoyynn0aL+DDOANmYle6xGO/K
le9v+/0CgYEA5nYvHKgv0YiPJTpDhw9lqJ1Resijy+OMMnDlTNjLMB4Wns5QWGLc
VlrShWMWYrInGS1d5Et6zNgUWjxxab2EAmMTkv6yJbuY6+kEu1EsYFdmy9bt9hlO
FQ2Yo7ICgODxpbhIyqaaQBaxc6WYIoYRw2oFp2Yvj4K7hhgEasKLLM8CgYEAxiOj
nfw9Fynjn3H/d9r7jvFAIeJsbH0GHkDfBZ0bEtbwvRLCib/5MelpjINhihgDnASk
6SwEf/xvhpacQk79f2Lx2cL+Wj/AK0v8E832NjqIB59pS7pk8nijcu8J6c0eQzAS
p8wkHhWVKnNsijjUEEnyY3tsbUuAbzVVdTA5UMcCgYBFeOMC1IB1vaDJLCMnF7Eh
fysMxGb8E4AzxGybGc9Glgtjm/YEbujU71P++bvJzMKUiGSBaW9/SLP577aQlZyx
y4QfD8BMN50FoJzYisPB1xcZ45SgV0h+eDbHQeYXS7gMqNzomghtwWmE3ypZXekE
63UA3YEA1fwJlDvgovypaQKBgQC0wVCDUNg+aHWCQNIo+jnhdk7mWpRFCG1rbgzH
J0LKlhE6u4GDfwGLuf8TM8vo2e15CHeVTBWy2Iy5gG5+w2bZLl+qJAw8MspR9Vi6
jHtfj1gHdDLv5dQvq0SZFl65zukbrCBouX/9ffz9pBzRn/Q+A+e/P5pzvpwlV8dl
SCARgwKBgFg0giQqEnXw9Xes+E3rsk0dRFUo0FBkDG7tG2eq0ekdw5MbS13r5NCA
uf07kcMQoo3m+VbB9EVGSFlrkWZ6LBwvUJArNbtimpi00lCGQ2HghuEf2H70crmT
pJUwMXRvoZpENDqfC8QOw8O53sNIx28hW+tmDX+o+ICQZlE6fwgn
-----END RSA PRIVATE KEY-----
ckim-mbp:temp ckim$ 
ckim-mbp:temp ckim$ openssl rsa -in myserver.com.key.pem -text -noout
Private-Key: (2048 bit)
modulus:
    00:b2:5f:7d:e4:14:8d:73:a6:9f:96:6b:34:17:e7:
    32:61:6f:84:8d:af:8a:b5:d6:92:be:e6:af:cc:ed:
    35:f4:69:1a:47:f2:7d:00:7d:38:4e:b3:29:e1:8e:
    1d:31:06:b4:e7:55:98:c1:56:ca:d8:7c:a1:e5:50:
    5a:e5:29:35:fb:1a:c6:e9:61:31:a6:ed:74:66:5a:
    d2:ad:35:5c:32:56:27:38:50:cf:7a:34:6c:05:06:
    1b:42:98:8b:c4:82:9a:e2:e8:73:23:41:47:db:1b:
    4e:39:37:d2:73:7e:62:04:ed:87:da:78:f9:11:95:
    14:03:aa:ff:8d:d0:79:0b:42:6e:8d:a1:28:51:a3:
    2c:1e:7c:bc:33:25:dd:c1:18:18:70:b5:6b:64:41:
    a8:72:ce:dc:87:d6:6f:aa:4e:b0:05:99:c4:ec:36:
    ca:a8:b9:2a:31:8d:a0:0a:82:bb:66:02:32:c5:7e:
    af:6e:91:27:fc:68:ef:6f:e5:6c:a6:71:0f:c1:62:
    d1:2a:b0:2f:b9:8c:80:7c:fc:61:b7:04:7f:1a:0d:
    54:26:ed:66:de:7d:d5:ec:65:ad:16:21:79:15:a6:
    3f:09:59:16:48:85:7d:4c:d9:3d:06:68:5c:4d:cd:
    84:0f:0c:5b:df:01:0e:b8:fa:e5:a3:6a:c7:82:47:
    84:e9
publicExponent: 65537 (0x10001)
privateExponent:
    3a:30:02:7e:5b:e2:04:ff:2f:02:3f:b8:7f:af:b0:
    f4:ae:0f:5c:b5:0e:17:e1:86:7f:75:fb:95:6b:30:
    75:a9:af:a4:16:cb:86:54:53:01:01:5b:41:34:3d:
    fb:97:47:7e:4b:a3:08:37:0a:f6:f2:39:51:f8:13:
    9e:bc:01:db:07:52:2a:21:c5:b3:c1:b4:7e:0b:54:
    bc:a2:32:90:4d:20:80:33:84:6b:46:1c:92:ca:fa:
    2b:90:5d:cf:de:17:2e:bc:4b:8b:0d:a9:a6:25:53:
    30:41:30:8a:f2:88:81:39:07:5f:52:a5:55:81:ff:
    44:6f:0c:ec:b3:3c:39:5a:87:aa:c4:05:6d:42:cd:
    5d:ba:26:a0:3e:f4:18:b1:11:cd:53:87:05:4c:c6:
    55:7c:a0:d5:55:95:67:5a:45:71:e9:81:10:dc:46:
    e7:1e:69:dd:64:04:6d:67:85:1c:bb:80:40:93:62:
    14:5a:23:d6:f0:d7:02:7d:33:5c:44:14:5a:12:8e:
    45:de:5a:f3:3e:0c:33:2a:33:19:0e:dd:ef:41:9c:
    13:7e:f7:58:7c:ee:35:cf:8d:40:66:7d:0b:77:b4:
    63:10:ba:d8:6b:1b:91:61:a3:2c:a7:9f:46:8b:f8:
    30:ce:00:d9:98:95:ee:b1:18:ef:ca:95:ef:6f:fb:
    fd
prime1:
    00:e6:76:2f:1c:a8:2f:d1:88:8f:25:3a:43:87:0f:
    65:a8:9d:51:7a:c8:a3:cb:e3:8c:32:70:e5:4c:d8:
    cb:30:1e:16:9e:ce:50:58:62:dc:56:5a:d2:85:63:
    16:62:b2:27:19:2d:5d:e4:4b:7a:cc:d8:14:5a:3c:
    71:69:bd:84:02:63:13:92:fe:b2:25:bb:98:eb:e9:
    04:bb:51:2c:60:57:66:cb:d6:ed:f6:19:4e:15:0d:
    98:a3:b2:02:80:e0:f1:a5:b8:48:ca:a6:9a:40:16:
    b1:73:a5:98:22:86:11:c3:6a:05:a7:66:2f:8f:82:
    bb:86:18:04:6a:c2:8b:2c:cf
prime2:
    00:c6:23:a3:9d:fc:3d:17:29:e3:9f:71:ff:77:da:
    fb:8e:f1:40:21:e2:6c:6c:7d:06:1e:40:df:05:9d:
    1b:12:d6:f0:bd:12:c2:89:bf:f9:31:e9:69:8c:83:
    61:8a:18:03:9c:04:a4:e9:2c:04:7f:fc:6f:86:96:
    9c:42:4e:fd:7f:62:f1:d9:c2:fe:5a:3f:c0:2b:4b:
    fc:13:cd:f6:36:3a:88:07:9f:69:4b:ba:64:f2:78:
    a3:72:ef:09:e9:cd:1e:43:30:12:a7:cc:24:1e:15:
    95:2a:73:6c:8a:38:d4:10:49:f2:63:7b:6c:6d:4b:
    80:6f:35:55:75:30:39:50:c7
exponent1:
    45:78:e3:02:d4:80:75:bd:a0:c9:2c:23:27:17:b1:
    21:7f:2b:0c:c4:66:fc:13:80:33:c4:6c:9b:19:cf:
    46:96:0b:63:9b:f6:04:6e:e8:d4:ef:53:fe:f9:bb:
    c9:cc:c2:94:88:64:81:69:6f:7f:48:b3:f9:ef:b6:
    90:95:9c:b1:cb:84:1f:0f:c0:4c:37:9d:05:a0:9c:
    d8:8a:c3:c1:d7:17:19:e3:94:a0:57:48:7e:78:36:
    c7:41:e6:17:4b:b8:0c:a8:dc:e8:9a:08:6d:c1:69:
    84:df:2a:59:5d:e9:04:eb:75:00:dd:81:00:d5:fc:
    09:94:3b:e0:a2:fc:a9:69
exponent2:
    00:b4:c1:50:83:50:d8:3e:68:75:82:40:d2:28:fa:
    39:e1:76:4e:e6:5a:94:45:08:6d:6b:6e:0c:c7:27:
    42:ca:96:11:3a:bb:81:83:7f:01:8b:b9:ff:13:33:
    cb:e8:d9:ed:79:08:77:95:4c:15:b2:d8:8c:b9:80:
    6e:7e:c3:66:d9:2e:5f:aa:24:0c:3c:32:ca:51:f5:
    58:ba:8c:7b:5f:8f:58:07:74:32:ef:e5:d4:2f:ab:
    44:99:16:5e:b9:ce:e9:1b:ac:20:68:b9:7f:fd:7d:
    fc:fd:a4:1c:d1:9f:f4:3e:03:e7:bf:3f:9a:73:be:
    9c:25:57:c7:65:48:20:11:83
coefficient:
    58:34:82:24:2a:12:75:f0:f5:77:ac:f8:4d:eb:b2:
    4d:1d:44:55:28:d0:50:64:0c:6e:ed:1b:67:aa:d1:
    e9:1d:c3:93:1b:4b:5d:eb:e4:d0:80:b9:fd:3b:91:
    c3:10:a2:8d:e6:f9:56:c1:f4:45:46:48:59:6b:91:
    66:7a:2c:1c:2f:50:90:2b:35:bb:62:9a:98:b4:d2:
    50:86:43:61:e0:86:e1:1f:d8:7e:f4:72:b9:93:a4:
    95:30:31:74:6f:a1:9a:44:34:3a:9f:0b:c4:0e:c3:
    c3:b9:de:c3:48:c7:6f:21:5b:eb:66:0d:7f:a8:f8:
    80:90:66:51:3a:7f:08:27
ckim-mbp:temp ckim$ 
```

### extract public key from the private key

```
ckim-mbp:temp ckim$ openssl rsa -in myserver.com.key.pem -pubout
writing RSA key
-----BEGIN PUBLIC KEY-----
MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAsl995BSNc6aflms0F+cy
YW+Eja+KtdaSvuavzO019GkaR/J9AH04TrMp4Y4dMQa051WYwVbK2Hyh5VBa5Sk1
+xrG6WExpu10ZlrSrTVcMlYnOFDPejRsBQYbQpiLxIKa4uhzI0FH2xtOOTfSc35i
BO2H2nj5EZUUA6r/jdB5C0JujaEoUaMsHny8MyXdwRgYcLVrZEGocs7ch9Zvqk6w
BZnE7DbKqLkqMY2gCoK7ZgIyxX6vbpEn/Gjvb+VspnEPwWLRKrAvuYyAfPxhtwR/
Gg1UJu1m3n3V7GWtFiF5FaY/CVkWSIV9TNk9BmhcTc2EDwxb3wEOuPrlo2rHgkeE
6QIDAQAB
-----END PUBLIC KEY-----
ckim-mbp:temp ckim$ 
```

### create CSR

```
ckim-mbp:temp ckim$ openssl req -nodes -new -key myserver.com.key.pem -out myserver.com.csr -subj "/C=US/ST=Mass/L=Westford/O=Juniper Net/OU=PC Cloud/CN=myserver.com"
ckim-mbp:temp ckim$ cat myserver.com.csr 
-----BEGIN CERTIFICATE REQUEST-----
MIICtDCCAZwCAQAwbzELMAkGA1UEBhMCVVMxDTALBgNVBAgTBE1hc3MxETAPBgNV
BAcTCFdlc3Rmb3JkMRQwEgYDVQQKEwtKdW5pcGVyIE5ldDERMA8GA1UECxMIUEMg
Q2xvdWQxFTATBgNVBAMTDG15c2VydmVyLmNvbTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBALJffeQUjXOmn5ZrNBfnMmFvhI2virXWkr7mr8ztNfRpGkfy
fQB9OE6zKeGOHTEGtOdVmMFWyth8oeVQWuUpNfsaxulhMabtdGZa0q01XDJWJzhQ
z3o0bAUGG0KYi8SCmuLocyNBR9sbTjk30nN+YgTth9p4+RGVFAOq/43QeQtCbo2h
KFGjLB58vDMl3cEYGHC1a2RBqHLO3IfWb6pOsAWZxOw2yqi5KjGNoAqCu2YCMsV+
r26RJ/xo72/lbKZxD8Fi0SqwL7mMgHz8YbcEfxoNVCbtZt591exlrRYheRWmPwlZ
FkiFfUzZPQZoXE3NhA8MW98BDrj65aNqx4JHhOkCAwEAAaAAMA0GCSqGSIb3DQEB
BQUAA4IBAQAx7sGiCsEV4iFCuICRQm+f+kEfWd9K1O2FsgQwfLDU+KznPEHBuKO1
i3jGwO6aG9YwSCuNoCETxbN3evfsfjStZLJ1nz5BUC7ew1tCjSLI/u3pwTr1UmHO
LpRTm7BbCDzxaYoWQvfxOrj8k7e3EjeKPJLXEkpxbrV70yptGcsXbGuiL9OujP0+
k00Ep5IY+xUKgXDugFY4wB5T4kxeHID46cTWacmZ6C4hZN01MohhCYXlMJ/jdN2b
0YvKiUZ/ZEc9hzq570yaELuQjuIWQk0HFy8etdAHZcaHrOhXVQvl1chN9EjhgxSm
Laml/cayN33GRHb/tvtmwtFCGxtCcUOB
-----END CERTIFICATE REQUEST-----
ckim-mbp:temp ckim$
ckim-mbp:temp ckim$ openssl req -in myserver.com.csr -text -noout    
Certificate Request:
    Data:
        Version: 0 (0x0)
        Subject: C=US, ST=Mass, L=Westford, O=Juniper Net, OU=PC Cloud, CN=myserver.com
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
            RSA Public Key: (2048 bit)
                Modulus (2048 bit):
                    00:b2:5f:7d:e4:14:8d:73:a6:9f:96:6b:34:17:e7:
                    32:61:6f:84:8d:af:8a:b5:d6:92:be:e6:af:cc:ed:
                    35:f4:69:1a:47:f2:7d:00:7d:38:4e:b3:29:e1:8e:
                    1d:31:06:b4:e7:55:98:c1:56:ca:d8:7c:a1:e5:50:
                    5a:e5:29:35:fb:1a:c6:e9:61:31:a6:ed:74:66:5a:
                    d2:ad:35:5c:32:56:27:38:50:cf:7a:34:6c:05:06:
                    1b:42:98:8b:c4:82:9a:e2:e8:73:23:41:47:db:1b:
                    4e:39:37:d2:73:7e:62:04:ed:87:da:78:f9:11:95:
                    14:03:aa:ff:8d:d0:79:0b:42:6e:8d:a1:28:51:a3:
                    2c:1e:7c:bc:33:25:dd:c1:18:18:70:b5:6b:64:41:
                    a8:72:ce:dc:87:d6:6f:aa:4e:b0:05:99:c4:ec:36:
                    ca:a8:b9:2a:31:8d:a0:0a:82:bb:66:02:32:c5:7e:
                    af:6e:91:27:fc:68:ef:6f:e5:6c:a6:71:0f:c1:62:
                    d1:2a:b0:2f:b9:8c:80:7c:fc:61:b7:04:7f:1a:0d:
                    54:26:ed:66:de:7d:d5:ec:65:ad:16:21:79:15:a6:
                    3f:09:59:16:48:85:7d:4c:d9:3d:06:68:5c:4d:cd:
                    84:0f:0c:5b:df:01:0e:b8:fa:e5:a3:6a:c7:82:47:
                    84:e9
                Exponent: 65537 (0x10001)
        Attributes:
            a0:00
    Signature Algorithm: sha1WithRSAEncryption
        31:ee:c1:a2:0a:c1:15:e2:21:42:b8:80:91:42:6f:9f:fa:41:
        1f:59:df:4a:d4:ed:85:b2:04:30:7c:b0:d4:f8:ac:e7:3c:41:
        c1:b8:a3:b5:8b:78:c6:c0:ee:9a:1b:d6:30:48:2b:8d:a0:21:
        13:c5:b3:77:7a:f7:ec:7e:34:ad:64:b2:75:9f:3e:41:50:2e:
        de:c3:5b:42:8d:22:c8:fe:ed:e9:c1:3a:f5:52:61:ce:2e:94:
        53:9b:b0:5b:08:3c:f1:69:8a:16:42:f7:f1:3a:b8:fc:93:b7:
        b7:12:37:8a:3c:92:d7:12:4a:71:6e:b5:7b:d3:2a:6d:19:cb:
        17:6c:6b:a2:2f:d3:ae:8c:fd:3e:93:4d:04:a7:92:18:fb:15:
        0a:81:70:ee:80:56:38:c0:1e:53:e2:4c:5e:1c:80:f8:e9:c4:
        d6:69:c9:99:e8:2e:21:64:dd:35:32:88:61:09:85:e5:30:9f:
        e3:74:dd:9b:d1:8b:ca:89:46:7f:64:47:3d:87:3a:b9:ef:4c:
        9a:10:bb:90:8e:e2:16:42:4d:07:17:2f:1e:b5:d0:07:65:c6:
        87:ac:e8:57:55:0b:e5:d5:c8:4d:f4:48:e1:83:14:a6:2d:a9:
        a5:fd:c6:b2:37:7d:c6:44:76:ff:b6:fb:66:c2:d1:42:1b:1b:
        42:71:43:81
ckim-mbp:temp ckim$ 
```


## example of certificate file
```
-----BEGIN CERTIFICATE-----
MIIGhzCCBW+gAwIBAgIRANVHM7SkM8EQAulRPIZ+sSowDQYJKoZIhvcNAQELBQAw
gZAxCzAJBgNVBAYTAkdCMRswGQYDVQQIExJHcmVhdGVyIE1hbmNoZXN0ZXIxEDAO
BgNVBAcTB1NhbGZvcmQxGjAYBgNVBAoTEUNPTU9ETyBDQSBMaW1pdGVkMTYwNAYD
VQQDEy1DT01PRE8gUlNBIERvbWFpbiBWYWxpZGF0aW9uIFNlY3VyZSBTZXJ2ZXIg
Q0EwHhcNMTgxMTA0MDAwMDAwWhcNMTkxMTA0MjM1OTU5WjBiMSEwHwYDVQQLExhE
b21haW4gQ29udHJvbCBWYWxpZGF0ZWQxFDASBgNVBAsTC1Bvc2l0aXZlU1NMMScw
JQYDVQQDEx5tYXN0ZXIub3MwMDEuam5wci1wcy1jbG91ZC5jb20wggEiMA0GCSqG
SIb3DQEBAQUAA4IBDwAwggEKAoIBAQCjqe7RX9Ob5b4eMuabFkqFM7DE+D7yP9CC
2qdwclCXsiRFPXFQ/Xo3f75w7FnWcIWBsWGzHkrF+JiFCNRYoD2aTJO76U1xkkDy
7V8heeTAPR30nQY3qr1Qg/WVclg+hIRBXC6wbDeeplysFpCd0R+jovRjHAxH9sRG
9IjMcSQvjoQXXQldjW8+vqjxxMRLt6NAoUwA3SQcfhJOJb3uHN2yrIiJiPCmgihD
0xreqiPgHLUYOIkp8Kx3WVIkOou0rJpT0h+A/vPvNEjdVLwiY939glgE+41rLsKa
PQvttS0tVdTbZdoNPD1ZVtZBHhEdXI0BvWxVN2jpJLXqklCtk5jpAgMBAAGjggMH
MIIDAzAfBgNVHSMEGDAWgBSQr2o6lFoL2JDqElZz30O0Oija5zAdBgNVHQ4EFgQU
X3yhfyA0/rhCTH+EO8XIahdLSpMwDgYDVR0PAQH/BAQDAgWgMAwGA1UdEwEB/wQC
MAAwHQYDVR0lBBYwFAYIKwYBBQUHAwEGCCsGAQUFBwMCME8GA1UdIARIMEYwOgYL
KwYBBAGyMQECAgcwKzApBggrBgEFBQcCARYdaHR0cHM6Ly9zZWN1cmUuY29tb2Rv
LmNvbS9DUFMwCAYGZ4EMAQIBMFQGA1UdHwRNMEswSaBHoEWGQ2h0dHA6Ly9jcmwu
Y29tb2RvY2EuY29tL0NPTU9ET1JTQURvbWFpblZhbGlkYXRpb25TZWN1cmVTZXJ2
ZXJDQS5jcmwwgYUGCCsGAQUFBwEBBHkwdzBPBggrBgEFBQcwAoZDaHR0cDovL2Ny
dC5jb21vZG9jYS5jb20vQ09NT0RPUlNBRG9tYWluVmFsaWRhdGlvblNlY3VyZVNl
cnZlckNBLmNydDAkBggrBgEFBQcwAYYYaHR0cDovL29jc3AuY29tb2RvY2EuY29t
ME0GA1UdEQRGMESCHm1hc3Rlci5vczAwMS5qbnByLXBzLWNsb3VkLmNvbYIid3d3
Lm1hc3Rlci5vczAwMS5qbnByLXBzLWNsb3VkLmNvbTCCAQQGCisGAQQB1nkCBAIE
gfUEgfIA8AB1AO5Lvbd1zmC64UJpH6vhnmajD35fsHLYgwDEe4l6qP3LAAABZt0o
ov8AAAQDAEYwRAIgDNp8PPFhyCBtwsdrbyiEiN5+/b/+6sylj53zOqU7zw4CID+8
axSIesCF94+JswPozvZhSzLTfzrls980iWD0+K2PAHcAdH7agzGtMxCRIZzOJU9C
cMK//V5CIAjGNzV55hB7zFYAAAFm3SijIgAABAMASDBGAiEA7ZUhHMSNWbNkd2zM
iD9S45D3/JHPNVt12nCuDt3KiacCIQDKWSkReA+v7uhZNFwET0hcL4yxbGNkRI6q
e+brcDec4jANBgkqhkiG9w0BAQsFAAOCAQEAfsk4Ws4psxDW1jpRjfDgcQzQKkyH
kl6RYYX+czZWzGVnmDrrzlapPcRRSGmziKrjGEHldmJkw/G3dmpdFLiZhfDhKpMD
XYVSl3gXj0gkhTZlthgjgaZDiv7AZ/Pes40FBZfHKLnnzg+E4nNGStJ03p8dC/KF
I9X7FI09P9I01LM+xyt51C3HJ9tWAy1HxyQmqYbm6Lf0VD4RA4lNO5j1u0k6awOr
Lin5ALDCTMxaiwKJTfU0t5IhE4STjLsWXJgy7Mk2TgzVderq2p2mYyW1SEFFeIYs
/XYI0s+yuorlh6UZEyuQBDZ6YcbYcSl8zjzvJvUekI4bujhv8Az66dDBlw==
-----END CERTIFICATE-----
```

```
ckim-mbp:temp ckim$ openssl x509 -in myserver.com.crt -text -noout
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            d5:47:33:b4:a4:33:c1:10:02:e9:51:3c:86:7e:b1:2a
        Signature Algorithm: sha256WithRSAEncryption
        Issuer: C=GB, ST=Greater Manchester, L=Salford, O=COMODO CA Limited, CN=COMODO RSA Domain Validation Secure Server CA
        Validity
            Not Before: Nov  4 00:00:00 2018 GMT
            Not After : Nov  4 23:59:59 2019 GMT
        Subject: OU=Domain Control Validated, OU=PositiveSSL, CN=master.os001.jnpr-ps-cloud.com
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
            RSA Public Key: (2048 bit)
                Modulus (2048 bit):
                    00:a3:a9:ee:d1:5f:d3:9b:e5:be:1e:32:e6:9b:16:
                    4a:85:33:b0:c4:f8:3e:f2:3f:d0:82:da:a7:70:72:
                    50:97:b2:24:45:3d:71:50:fd:7a:37:7f:be:70:ec:
                    59:d6:70:85:81:b1:61:b3:1e:4a:c5:f8:98:85:08:
                    d4:58:a0:3d:9a:4c:93:bb:e9:4d:71:92:40:f2:ed:
                    5f:21:79:e4:c0:3d:1d:f4:9d:06:37:aa:bd:50:83:
                    f5:95:72:58:3e:84:84:41:5c:2e:b0:6c:37:9e:a6:
                    5c:ac:16:90:9d:d1:1f:a3:a2:f4:63:1c:0c:47:f6:
                    c4:46:f4:88:cc:71:24:2f:8e:84:17:5d:09:5d:8d:
                    6f:3e:be:a8:f1:c4:c4:4b:b7:a3:40:a1:4c:00:dd:
                    24:1c:7e:12:4e:25:bd:ee:1c:dd:b2:ac:88:89:88:
                    f0:a6:82:28:43:d3:1a:de:aa:23:e0:1c:b5:18:38:
                    89:29:f0:ac:77:59:52:24:3a:8b:b4:ac:9a:53:d2:
                    1f:80:fe:f3:ef:34:48:dd:54:bc:22:63:dd:fd:82:
                    58:04:fb:8d:6b:2e:c2:9a:3d:0b:ed:b5:2d:2d:55:
                    d4:db:65:da:0d:3c:3d:59:56:d6:41:1e:11:1d:5c:
                    8d:01:bd:6c:55:37:68:e9:24:b5:ea:92:50:ad:93:
                    98:e9
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Authority Key Identifier: 
                keyid:90:AF:6A:3A:94:5A:0B:D8:90:EA:12:56:73:DF:43:B4:3A:28:DA:E7

            X509v3 Subject Key Identifier: 
                5F:7C:A1:7F:20:34:FE:B8:42:4C:7F:84:3B:C5:C8:6A:17:4B:4A:93
            X509v3 Key Usage: critical
                Digital Signature, Key Encipherment
            X509v3 Basic Constraints: critical
                CA:FALSE
            X509v3 Extended Key Usage: 
                TLS Web Server Authentication, TLS Web Client Authentication
            X509v3 Certificate Policies: 
                Policy: 1.3.6.1.4.1.6449.1.2.2.7
                  CPS: https://secure.comodo.com/CPS
                Policy: 2.23.140.1.2.1

            X509v3 CRL Distribution Points: 
                URI:http://crl.comodoca.com/COMODORSADomainValidationSecureServerCA.crl

            Authority Information Access: 
                CA Issuers - URI:http://crt.comodoca.com/COMODORSADomainValidationSecureServerCA.crt
                OCSP - URI:http://ocsp.comodoca.com

            X509v3 Subject Alternative Name: 
                DNS:master.os001.jnpr-ps-cloud.com, DNS:www.master.os001.jnpr-ps-cloud.com
            1.3.6.1.4.1.11129.2.4.2: 
                ......u..K..u.`..Bi....f..~_.r....{.z......f.(.......F0D. ..|<.a. m..ko(...~.........:.;... ?.k..z..........aK2..:...4.`.....w.t~..1.3..!..%OBp...^B ..75y..{.V...f.(.".....H0F.!...!...Y.dwl..?R......5[u.p.......!..Y).x....Y4\.OH\/..lcdD..{..p7..
    Signature Algorithm: sha256WithRSAEncryption
        7e:c9:38:5a:ce:29:b3:10:d6:d6:3a:51:8d:f0:e0:71:0c:d0:
        2a:4c:87:92:5e:91:61:85:fe:73:36:56:cc:65:67:98:3a:eb:
        ce:56:a9:3d:c4:51:48:69:b3:88:aa:e3:18:41:e5:76:62:64:
        c3:f1:b7:76:6a:5d:14:b8:99:85:f0:e1:2a:93:03:5d:85:52:
        97:78:17:8f:48:24:85:36:65:b6:18:23:81:a6:43:8a:fe:c0:
        67:f3:de:b3:8d:05:05:97:c7:28:b9:e7:ce:0f:84:e2:73:46:
        4a:d2:74:de:9f:1d:0b:f2:85:23:d5:fb:14:8d:3d:3f:d2:34:
        d4:b3:3e:c7:2b:79:d4:2d:c7:27:db:56:03:2d:47:c7:24:26:
        a9:86:e6:e8:b7:f4:54:3e:11:03:89:4d:3b:98:f5:bb:49:3a:
        6b:03:ab:2e:29:f9:00:b0:c2:4c:cc:5a:8b:02:89:4d:f5:34:
        b7:92:21:13:84:93:8c:bb:16:5c:98:32:ec:c9:36:4e:0c:d5:
        75:ea:ea:da:9d:a6:63:25:b5:48:41:45:78:86:2c:fd:76:08:
        d2:cf:b2:ba:8a:e5:87:a5:19:13:2b:90:04:36:7a:61:c6:d8:
        71:29:7c:ce:3c:ef:26:f5:1e:90:8e:1b:ba:38:6f:f0:0c:fa:
        e9:d0:c1:97
ckim-mbp:temp ckim$ 
```


## example of certificate bundle
```
-----BEGIN CERTIFICATE-----
MIIGCDCCA/CgAwIBAgIQKy5u6tl1NmwUim7bo3yMBzANBgkqhkiG9w0BAQwFADCB
hTELMAkGA1UEBhMCR0IxGzAZBgNVBAgTEkdyZWF0ZXIgTWFuY2hlc3RlcjEQMA4G
A1UEBxMHU2FsZm9yZDEaMBgGA1UEChMRQ09NT0RPIENBIExpbWl0ZWQxKzApBgNV
BAMTIkNPTU9ETyBSU0EgQ2VydGlmaWNhdGlvbiBBdXRob3JpdHkwHhcNMTQwMjEy
MDAwMDAwWhcNMjkwMjExMjM1OTU5WjCBkDELMAkGA1UEBhMCR0IxGzAZBgNVBAgT
EkdyZWF0ZXIgTWFuY2hlc3RlcjEQMA4GA1UEBxMHU2FsZm9yZDEaMBgGA1UEChMR
Q09NT0RPIENBIExpbWl0ZWQxNjA0BgNVBAMTLUNPTU9ETyBSU0EgRG9tYWluIFZh
bGlkYXRpb24gU2VjdXJlIFNlcnZlciBDQTCCASIwDQYJKoZIhvcNAQEBBQADggEP
ADCCAQoCggEBAI7CAhnhoFmk6zg1jSz9AdDTScBkxwtiBUUWOqigwAwCfx3M28Sh
bXcDow+G+eMGnD4LgYqbSRutA776S9uMIO3Vzl5ljj4Nr0zCsLdFXlIvNN5IJGS0
Qa4Al/e+Z96e0HqnU4A7fK31llVvl0cKfIWLIpeNs4TgllfQcBhglo/uLQeTnaG6
ytHNe+nEKpooIZFNb5JPJaXyejXdJtxGpdCsWTWM/06RQ1A/WZMebFEh7lgUq/51
UHg+TLAchhP6a5i84DuUHoVS3AOTJBhuyydRReZw3iVDpA3hSqXttn7IzW3uLh0n
c13cRTCAquOyQQuvvUSH2rnlG51/ruWFgqUCAwEAAaOCAWUwggFhMB8GA1UdIwQY
MBaAFLuvfgI9+qbxPISOre44mOzZMjLUMB0GA1UdDgQWBBSQr2o6lFoL2JDqElZz
30O0Oija5zAOBgNVHQ8BAf8EBAMCAYYwEgYDVR0TAQH/BAgwBgEB/wIBADAdBgNV
HSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwGwYDVR0gBBQwEjAGBgRVHSAAMAgG
BmeBDAECATBMBgNVHR8ERTBDMEGgP6A9hjtodHRwOi8vY3JsLmNvbW9kb2NhLmNv
bS9DT01PRE9SU0FDZXJ0aWZpY2F0aW9uQXV0aG9yaXR5LmNybDBxBggrBgEFBQcB
AQRlMGMwOwYIKwYBBQUHMAKGL2h0dHA6Ly9jcnQuY29tb2RvY2EuY29tL0NPTU9E
T1JTQUFkZFRydXN0Q0EuY3J0MCQGCCsGAQUFBzABhhhodHRwOi8vb2NzcC5jb21v
ZG9jYS5jb20wDQYJKoZIhvcNAQEMBQADggIBAE4rdk+SHGI2ibp3wScF9BzWRJ2p
mj6q1WZmAT7qSeaiNbz69t2Vjpk1mA42GHWx3d1Qcnyu3HeIzg/3kCDKo2cuH1Z/
e+FE6kKVxF0NAVBGFfKBiVlsit2M8RKhjTpCipj4SzR7JzsItG8kO3KdY3RYPBps
P0/HEZrIqPW1N+8QRcZs2eBelSaz662jue5/DJpmNXMyYE7l3YphLG5SEXdoltMY
dVEVABt0iN3hxzgEQyjpFv3ZBdRdRydg1vs4O2xyopT4Qhrf7W8GjEXCBgCq5Ojc
2bXhc3js9iPc0d1sjhqPpepUfJa3w/5Vjo1JXvxku88+vZbrac2/4EjxYoIQ5QxG
V/Iz2tDIY+3GH5QFlkoakdH368+PUq4NCNk+qKBR6cGHdNXJ93SrLlP7u3r7l+L4
HyaPs9Kg4DdbKDsx5Q5XLVq4rXmsXiBmGqW5prU5wfWYQ//u+aen/e7KJD2AFsQX
j4rBYKEMrltDR5FL1ZoXX/nUh8HCjLfn4g8wGTeGrODcQgPmlKidrv0PJFGUzpII
0fxQ8ANAe4hZ7Q7drNJ3gjTcBpUC2JD5Leo31Rpg0Gcg19hCC0Wvgmje3WYkN5Ap
lBlGGSW4gNfL1IYoakRwJiNiqZ+Gb7+6kHDSVneFeO/qJakXzlByjAA6quPbYzSf
+AZxAeKCINT+b72x
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIFdDCCBFygAwIBAgIQJ2buVutJ846r13Ci/ITeIjANBgkqhkiG9w0BAQwFADBv
MQswCQYDVQQGEwJTRTEUMBIGA1UEChMLQWRkVHJ1c3QgQUIxJjAkBgNVBAsTHUFk
ZFRydXN0IEV4dGVybmFsIFRUUCBOZXR3b3JrMSIwIAYDVQQDExlBZGRUcnVzdCBF
eHRlcm5hbCBDQSBSb290MB4XDTAwMDUzMDEwNDgzOFoXDTIwMDUzMDEwNDgzOFow
gYUxCzAJBgNVBAYTAkdCMRswGQYDVQQIExJHcmVhdGVyIE1hbmNoZXN0ZXIxEDAO
BgNVBAcTB1NhbGZvcmQxGjAYBgNVBAoTEUNPTU9ETyBDQSBMaW1pdGVkMSswKQYD
VQQDEyJDT01PRE8gUlNBIENlcnRpZmljYXRpb24gQXV0aG9yaXR5MIICIjANBgkq
hkiG9w0BAQEFAAOCAg8AMIICCgKCAgEAkehUktIKVrGsDSTdxc9EZ3SZKzejfSNw
AHG8U9/E+ioSj0t/EFa9n3Byt2F/yUsPF6c947AEYe7/EZfH9IY+Cvo+XPmT5jR6
2RRr55yzhaCCenavcZDX7P0N+pxs+t+wgvQUfvm+xKYvT3+Zf7X8Z0NyvQwA1onr
ayzT7Y+YHBSrfuXjbvzYqOSSJNpDa2K4Vf3qwbxstovzDo2a5JtsaZn4eEgwRdWt
4Q08RWD8MpZRJ7xnw8outmvqRsfHIKCxH2XeSAi6pE6p8oNGN4Tr6MyBSENnTnIq
m1y9TBsoilwie7SrmNnu4FGDwwlGTm0+mfqVF9p8M1dBPI1R7Qu2XK8sYxrfV8g/
vOldxJuvRZnio1oktLqpVj3Pb6r/SVi+8Kj/9Lit6Tf7urj0Czr56ENCHonYhMsT
8dm74YlguIwoVqwUHZwK53Hrzw7dPamWoUi9PPevtQ0iTMARgexWO/bTouJbt7IE
IlKVgJNp6I5MZfGRAy1wdALqi2cVKWlSArvX31BqVUa/oKMoYX9w0MOiqiwhqkfO
KJwGRXa/ghgntNWutMtQ5mv0TIZxMOmm3xaG4Nj/QN370EKIf6MzOi5cHkERgWPO
GHFrK+ymircxXDpqR+DDeVnWIBqv8mqYqnK8V0rSS527EPywTEHl7R09XiidnMy/
s1Hap0flhFMCAwEAAaOB9DCB8TAfBgNVHSMEGDAWgBStvZh6NLQm9/rEJlTvA73g
JMtUGjAdBgNVHQ4EFgQUu69+Aj36pvE8hI6t7jiY7NkyMtQwDgYDVR0PAQH/BAQD
AgGGMA8GA1UdEwEB/wQFMAMBAf8wEQYDVR0gBAowCDAGBgRVHSAAMEQGA1UdHwQ9
MDswOaA3oDWGM2h0dHA6Ly9jcmwudXNlcnRydXN0LmNvbS9BZGRUcnVzdEV4dGVy
bmFsQ0FSb290LmNybDA1BggrBgEFBQcBAQQpMCcwJQYIKwYBBQUHMAGGGWh0dHA6
Ly9vY3NwLnVzZXJ0cnVzdC5jb20wDQYJKoZIhvcNAQEMBQADggEBAGS/g/FfmoXQ
zbihKVcN6Fr30ek+8nYEbvFScLsePP9NDXRqzIGCJdPDoCpdTPW6i6FtxFQJdcfj
Jw5dhHk3QBN39bSsHNA7qxcS1u80GH4r6XnTq1dFDK8o+tDb5VCViLvfhVdpfZLY
Uspzgb8c8+a4bmYRBbMelC1/kZWSWfFMzqORcUx8Rww7Cxn2obFshj5cqsQugsv5
B5a6SE2Q8pTIqXOi6wZ7I53eovNNVZ96YUWYGGjHXkBrI/V5eu+MtWuLt29G9Hvx
PUsE2JOAWVrgQSQdso8VYFhH2+9uRv0V9dlfmrPb2LjkQLPNlzmuhbsdjrzch5vR
pu/xO28QOG8=
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIENjCCAx6gAwIBAgIBATANBgkqhkiG9w0BAQUFADBvMQswCQYDVQQGEwJTRTEU
MBIGA1UEChMLQWRkVHJ1c3QgQUIxJjAkBgNVBAsTHUFkZFRydXN0IEV4dGVybmFs
IFRUUCBOZXR3b3JrMSIwIAYDVQQDExlBZGRUcnVzdCBFeHRlcm5hbCBDQSBSb290
MB4XDTAwMDUzMDEwNDgzOFoXDTIwMDUzMDEwNDgzOFowbzELMAkGA1UEBhMCU0Ux
FDASBgNVBAoTC0FkZFRydXN0IEFCMSYwJAYDVQQLEx1BZGRUcnVzdCBFeHRlcm5h
bCBUVFAgTmV0d29yazEiMCAGA1UEAxMZQWRkVHJ1c3QgRXh0ZXJuYWwgQ0EgUm9v
dDCCASIwDQYJKoZIhvcNAQEBBQADggEPADCCAQoCggEBALf3GjPm8gAELTngTlvt
H7xsD821+iO2zt6bETOXpClMfZOfvUq8k+0DGuOPz+VtUFrWlymUWoCwSXrbLpX9
uMq/NzgtHj6RQa1wVsfwTz/oMp50ysiQVOnGXw94nZpAPA6sYapeFI+eh6FqUNzX
mk6vBbOmcZSccbNQYArHE504B4YCqOmoaSYYkKtMsE8jqzpPhNjfzp/haW+710LX
a0Tkx63ubUFfclpxCDezeWWkWaCUN/cALw3CknLa0Dhy2xSoRcRdKn23tNbE7qzN
E0S3ySvdQwAl+mG5aWpYIxG3pzOPVnVZ9c0p10a3CitlttNCbxWyuHv77+ldU9U0
WicCAwEAAaOB3DCB2TAdBgNVHQ4EFgQUrb2YejS0Jvf6xCZU7wO94CTLVBowCwYD
VR0PBAQDAgEGMA8GA1UdEwEB/wQFMAMBAf8wgZkGA1UdIwSBkTCBjoAUrb2YejS0
Jvf6xCZU7wO94CTLVBqhc6RxMG8xCzAJBgNVBAYTAlNFMRQwEgYDVQQKEwtBZGRU
cnVzdCBBQjEmMCQGA1UECxMdQWRkVHJ1c3QgRXh0ZXJuYWwgVFRQIE5ldHdvcmsx
IjAgBgNVBAMTGUFkZFRydXN0IEV4dGVybmFsIENBIFJvb3SCAQEwDQYJKoZIhvcN
AQEFBQADggEBALCb4IUlwtYj4g+WBpKdQZic2YR5gdkeWxQHIzZlj7DYd7usQWxH
YINRsPkyPef89iYTx4AWpb9a/IfPeHmJIZriTAcKhjW88t5RxNKWt9x+Tu5w/Rw5
6wwCURQtjr0W4MHfRnXnJK3s9EK0hZNwEGe6nQY1ShjTK3rMUUKhemPR5ruhxSvC
Nr4TDea9Y355e6cJDUCrat2PisP29owaQgVR1EX1n6diIWgVIEM8med8vSTYqZEX
c4g/VhsxOBi0cQ+azcgOno4uG+GMmIPLHzHxREzGBHNJdmAPx/i9F4BrLunMTA5a
mnkPIAou1Z5jJh5VkpTYghdae9C8x49OhgQ=
-----END CERTIFICATE-----
```

```
ckim-mbp:temp ckim$ openssl x509 -in myserver.bundle -text -noout
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            2b:2e:6e:ea:d9:75:36:6c:14:8a:6e:db:a3:7c:8c:07
        Signature Algorithm: sha384WithRSAEncryption
        Issuer: C=GB, ST=Greater Manchester, L=Salford, O=COMODO CA Limited, CN=COMODO RSA Certification Authority
        Validity
            Not Before: Feb 12 00:00:00 2014 GMT
            Not After : Feb 11 23:59:59 2029 GMT
        Subject: C=GB, ST=Greater Manchester, L=Salford, O=COMODO CA Limited, CN=COMODO RSA Domain Validation Secure Server CA
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
            RSA Public Key: (2048 bit)
                Modulus (2048 bit):
                    00:8e:c2:02:19:e1:a0:59:a4:eb:38:35:8d:2c:fd:
                    01:d0:d3:49:c0:64:c7:0b:62:05:45:16:3a:a8:a0:
                    c0:0c:02:7f:1d:cc:db:c4:a1:6d:77:03:a3:0f:86:
                    f9:e3:06:9c:3e:0b:81:8a:9b:49:1b:ad:03:be:fa:
                    4b:db:8c:20:ed:d5:ce:5e:65:8e:3e:0d:af:4c:c2:
                    b0:b7:45:5e:52:2f:34:de:48:24:64:b4:41:ae:00:
                    97:f7:be:67:de:9e:d0:7a:a7:53:80:3b:7c:ad:f5:
                    96:55:6f:97:47:0a:7c:85:8b:22:97:8d:b3:84:e0:
                    96:57:d0:70:18:60:96:8f:ee:2d:07:93:9d:a1:ba:
                    ca:d1:cd:7b:e9:c4:2a:9a:28:21:91:4d:6f:92:4f:
                    25:a5:f2:7a:35:dd:26:dc:46:a5:d0:ac:59:35:8c:
                    ff:4e:91:43:50:3f:59:93:1e:6c:51:21:ee:58:14:
                    ab:fe:75:50:78:3e:4c:b0:1c:86:13:fa:6b:98:bc:
                    e0:3b:94:1e:85:52:dc:03:93:24:18:6e:cb:27:51:
                    45:e6:70:de:25:43:a4:0d:e1:4a:a5:ed:b6:7e:c8:
                    cd:6d:ee:2e:1d:27:73:5d:dc:45:30:80:aa:e3:b2:
                    41:0b:af:bd:44:87:da:b9:e5:1b:9d:7f:ae:e5:85:
                    82:a5
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Authority Key Identifier: 
                keyid:BB:AF:7E:02:3D:FA:A6:F1:3C:84:8E:AD:EE:38:98:EC:D9:32:32:D4

            X509v3 Subject Key Identifier: 
                90:AF:6A:3A:94:5A:0B:D8:90:EA:12:56:73:DF:43:B4:3A:28:DA:E7
            X509v3 Key Usage: critical
                Digital Signature, Certificate Sign, CRL Sign
            X509v3 Basic Constraints: critical
                CA:TRUE, pathlen:0
            X509v3 Extended Key Usage: 
                TLS Web Server Authentication, TLS Web Client Authentication
            X509v3 Certificate Policies: 
                Policy: X509v3 Any Policy
                Policy: 2.23.140.1.2.1

            X509v3 CRL Distribution Points: 
                URI:http://crl.comodoca.com/COMODORSACertificationAuthority.crl

            Authority Information Access: 
                CA Issuers - URI:http://crt.comodoca.com/COMODORSAAddTrustCA.crt
                OCSP - URI:http://ocsp.comodoca.com

    Signature Algorithm: sha384WithRSAEncryption
        4e:2b:76:4f:92:1c:62:36:89:ba:77:c1:27:05:f4:1c:d6:44:
        9d:a9:9a:3e:aa:d5:66:66:01:3e:ea:49:e6:a2:35:bc:fa:f6:
        dd:95:8e:99:35:98:0e:36:18:75:b1:dd:dd:50:72:7c:ae:dc:
        77:88:ce:0f:f7:90:20:ca:a3:67:2e:1f:56:7f:7b:e1:44:ea:
        42:95:c4:5d:0d:01:50:46:15:f2:81:89:59:6c:8a:dd:8c:f1:
        12:a1:8d:3a:42:8a:98:f8:4b:34:7b:27:3b:08:b4:6f:24:3b:
        72:9d:63:74:58:3c:1a:6c:3f:4f:c7:11:9a:c8:a8:f5:b5:37:
        ef:10:45:c6:6c:d9:e0:5e:95:26:b3:eb:ad:a3:b9:ee:7f:0c:
        9a:66:35:73:32:60:4e:e5:dd:8a:61:2c:6e:52:11:77:68:96:
        d3:18:75:51:15:00:1b:74:88:dd:e1:c7:38:04:43:28:e9:16:
        fd:d9:05:d4:5d:47:27:60:d6:fb:38:3b:6c:72:a2:94:f8:42:
        1a:df:ed:6f:06:8c:45:c2:06:00:aa:e4:e8:dc:d9:b5:e1:73:
        78:ec:f6:23:dc:d1:dd:6c:8e:1a:8f:a5:ea:54:7c:96:b7:c3:
        fe:55:8e:8d:49:5e:fc:64:bb:cf:3e:bd:96:eb:69:cd:bf:e0:
        48:f1:62:82:10:e5:0c:46:57:f2:33:da:d0:c8:63:ed:c6:1f:
        94:05:96:4a:1a:91:d1:f7:eb:cf:8f:52:ae:0d:08:d9:3e:a8:
        a0:51:e9:c1:87:74:d5:c9:f7:74:ab:2e:53:fb:bb:7a:fb:97:
        e2:f8:1f:26:8f:b3:d2:a0:e0:37:5b:28:3b:31:e5:0e:57:2d:
        5a:b8:ad:79:ac:5e:20:66:1a:a5:b9:a6:b5:39:c1:f5:98:43:
        ff:ee:f9:a7:a7:fd:ee:ca:24:3d:80:16:c4:17:8f:8a:c1:60:
        a1:0c:ae:5b:43:47:91:4b:d5:9a:17:5f:f9:d4:87:c1:c2:8c:
        b7:e7:e2:0f:30:19:37:86:ac:e0:dc:42:03:e6:94:a8:9d:ae:
        fd:0f:24:51:94:ce:92:08:d1:fc:50:f0:03:40:7b:88:59:ed:
        0e:dd:ac:d2:77:82:34:dc:06:95:02:d8:90:f9:2d:ea:37:d5:
        1a:60:d0:67:20:d7:d8:42:0b:45:af:82:68:de:dd:66:24:37:
        90:29:94:19:46:19:25:b8:80:d7:cb:d4:86:28:6a:44:70:26:
        23:62:a9:9f:86:6f:bf:ba:90:70:d2:56:77:85:78:ef:ea:25:
        a9:17:ce:50:72:8c:00:3a:aa:e3:db:63:34:9f:f8:06:71:01:
        e2:82:20:d4:fe:6f:bd:b1
ckim-mbp:temp ckim$ 

ckim-mbp:temp ckim$ openssl x509 -in b -text
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number:
            27:66:ee:56:eb:49:f3:8e:ab:d7:70:a2:fc:84:de:22
        Signature Algorithm: sha384WithRSAEncryption
        Issuer: C=SE, O=AddTrust AB, OU=AddTrust External TTP Network, CN=AddTrust External CA Root
        Validity
            Not Before: May 30 10:48:38 2000 GMT
            Not After : May 30 10:48:38 2020 GMT
        Subject: C=GB, ST=Greater Manchester, L=Salford, O=COMODO CA Limited, CN=COMODO RSA Certification Authority
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
            RSA Public Key: (4096 bit)
                Modulus (4096 bit):
                    00:91:e8:54:92:d2:0a:56:b1:ac:0d:24:dd:c5:cf:
                    44:67:74:99:2b:37:a3:7d:23:70:00:71:bc:53:df:
                    c4:fa:2a:12:8f:4b:7f:10:56:bd:9f:70:72:b7:61:
                    7f:c9:4b:0f:17:a7:3d:e3:b0:04:61:ee:ff:11:97:
                    c7:f4:86:3e:0a:fa:3e:5c:f9:93:e6:34:7a:d9:14:
                    6b:e7:9c:b3:85:a0:82:7a:76:af:71:90:d7:ec:fd:
                    0d:fa:9c:6c:fa:df:b0:82:f4:14:7e:f9:be:c4:a6:
                    2f:4f:7f:99:7f:b5:fc:67:43:72:bd:0c:00:d6:89:
                    eb:6b:2c:d3:ed:8f:98:1c:14:ab:7e:e5:e3:6e:fc:
                    d8:a8:e4:92:24:da:43:6b:62:b8:55:fd:ea:c1:bc:
                    6c:b6:8b:f3:0e:8d:9a:e4:9b:6c:69:99:f8:78:48:
                    30:45:d5:ad:e1:0d:3c:45:60:fc:32:96:51:27:bc:
                    67:c3:ca:2e:b6:6b:ea:46:c7:c7:20:a0:b1:1f:65:
                    de:48:08:ba:a4:4e:a9:f2:83:46:37:84:eb:e8:cc:
                    81:48:43:67:4e:72:2a:9b:5c:bd:4c:1b:28:8a:5c:
                    22:7b:b4:ab:98:d9:ee:e0:51:83:c3:09:46:4e:6d:
                    3e:99:fa:95:17:da:7c:33:57:41:3c:8d:51:ed:0b:
                    b6:5c:af:2c:63:1a:df:57:c8:3f:bc:e9:5d:c4:9b:
                    af:45:99:e2:a3:5a:24:b4:ba:a9:56:3d:cf:6f:aa:
                    ff:49:58:be:f0:a8:ff:f4:b8:ad:e9:37:fb:ba:b8:
                    f4:0b:3a:f9:e8:43:42:1e:89:d8:84:cb:13:f1:d9:
                    bb:e1:89:60:b8:8c:28:56:ac:14:1d:9c:0a:e7:71:
                    eb:cf:0e:dd:3d:a9:96:a1:48:bd:3c:f7:af:b5:0d:
                    22:4c:c0:11:81:ec:56:3b:f6:d3:a2:e2:5b:b7:b2:
                    04:22:52:95:80:93:69:e8:8e:4c:65:f1:91:03:2d:
                    70:74:02:ea:8b:67:15:29:69:52:02:bb:d7:df:50:
                    6a:55:46:bf:a0:a3:28:61:7f:70:d0:c3:a2:aa:2c:
                    21:aa:47:ce:28:9c:06:45:76:bf:82:18:27:b4:d5:
                    ae:b4:cb:50:e6:6b:f4:4c:86:71:30:e9:a6:df:16:
                    86:e0:d8:ff:40:dd:fb:d0:42:88:7f:a3:33:3a:2e:
                    5c:1e:41:11:81:63:ce:18:71:6b:2b:ec:a6:8a:b7:
                    31:5c:3a:6a:47:e0:c3:79:59:d6:20:1a:af:f2:6a:
                    98:aa:72:bc:57:4a:d2:4b:9d:bb:10:fc:b0:4c:41:
                    e5:ed:1d:3d:5e:28:9d:9c:cc:bf:b3:51:da:a7:47:
                    e5:84:53
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Authority Key Identifier: 
                keyid:AD:BD:98:7A:34:B4:26:F7:FA:C4:26:54:EF:03:BD:E0:24:CB:54:1A

            X509v3 Subject Key Identifier: 
                BB:AF:7E:02:3D:FA:A6:F1:3C:84:8E:AD:EE:38:98:EC:D9:32:32:D4
            X509v3 Key Usage: critical
                Digital Signature, Certificate Sign, CRL Sign
            X509v3 Basic Constraints: critical
                CA:TRUE
            X509v3 Certificate Policies: 
                Policy: X509v3 Any Policy

            X509v3 CRL Distribution Points: 
                URI:http://crl.usertrust.com/AddTrustExternalCARoot.crl

            Authority Information Access: 
                OCSP - URI:http://ocsp.usertrust.com

    Signature Algorithm: sha384WithRSAEncryption
        64:bf:83:f1:5f:9a:85:d0:cd:b8:a1:29:57:0d:e8:5a:f7:d1:
        e9:3e:f2:76:04:6e:f1:52:70:bb:1e:3c:ff:4d:0d:74:6a:cc:
        81:82:25:d3:c3:a0:2a:5d:4c:f5:ba:8b:a1:6d:c4:54:09:75:
        c7:e3:27:0e:5d:84:79:37:40:13:77:f5:b4:ac:1c:d0:3b:ab:
        17:12:d6:ef:34:18:7e:2b:e9:79:d3:ab:57:45:0c:af:28:fa:
        d0:db:e5:50:95:88:bb:df:85:57:69:7d:92:d8:52:ca:73:81:
        bf:1c:f3:e6:b8:6e:66:11:05:b3:1e:94:2d:7f:91:95:92:59:
        f1:4c:ce:a3:91:71:4c:7c:47:0c:3b:0b:19:f6:a1:b1:6c:86:
        3e:5c:aa:c4:2e:82:cb:f9:07:96:ba:48:4d:90:f2:94:c8:a9:
        73:a2:eb:06:7b:23:9d:de:a2:f3:4d:55:9f:7a:61:45:98:18:
        68:c7:5e:40:6b:23:f5:79:7a:ef:8c:b5:6b:8b:b7:6f:46:f4:
        7b:f1:3d:4b:04:d8:93:80:59:5a:e0:41:24:1d:b2:8f:15:60:
        58:47:db:ef:6e:46:fd:15:f5:d9:5f:9a:b3:db:d8:b8:e4:40:
        b3:cd:97:39:ae:85:bb:1d:8e:bc:dc:87:9b:d1:a6:ef:f1:3b:
        6f:10:38:6f
-----BEGIN CERTIFICATE-----
MIIFdDCCBFygAwIBAgIQJ2buVutJ846r13Ci/ITeIjANBgkqhkiG9w0BAQwFADBv
MQswCQYDVQQGEwJTRTEUMBIGA1UEChMLQWRkVHJ1c3QgQUIxJjAkBgNVBAsTHUFk
ZFRydXN0IEV4dGVybmFsIFRUUCBOZXR3b3JrMSIwIAYDVQQDExlBZGRUcnVzdCBF
eHRlcm5hbCBDQSBSb290MB4XDTAwMDUzMDEwNDgzOFoXDTIwMDUzMDEwNDgzOFow
gYUxCzAJBgNVBAYTAkdCMRswGQYDVQQIExJHcmVhdGVyIE1hbmNoZXN0ZXIxEDAO
BgNVBAcTB1NhbGZvcmQxGjAYBgNVBAoTEUNPTU9ETyBDQSBMaW1pdGVkMSswKQYD
VQQDEyJDT01PRE8gUlNBIENlcnRpZmljYXRpb24gQXV0aG9yaXR5MIICIjANBgkq
hkiG9w0BAQEFAAOCAg8AMIICCgKCAgEAkehUktIKVrGsDSTdxc9EZ3SZKzejfSNw
AHG8U9/E+ioSj0t/EFa9n3Byt2F/yUsPF6c947AEYe7/EZfH9IY+Cvo+XPmT5jR6
2RRr55yzhaCCenavcZDX7P0N+pxs+t+wgvQUfvm+xKYvT3+Zf7X8Z0NyvQwA1onr
ayzT7Y+YHBSrfuXjbvzYqOSSJNpDa2K4Vf3qwbxstovzDo2a5JtsaZn4eEgwRdWt
4Q08RWD8MpZRJ7xnw8outmvqRsfHIKCxH2XeSAi6pE6p8oNGN4Tr6MyBSENnTnIq
m1y9TBsoilwie7SrmNnu4FGDwwlGTm0+mfqVF9p8M1dBPI1R7Qu2XK8sYxrfV8g/
vOldxJuvRZnio1oktLqpVj3Pb6r/SVi+8Kj/9Lit6Tf7urj0Czr56ENCHonYhMsT
8dm74YlguIwoVqwUHZwK53Hrzw7dPamWoUi9PPevtQ0iTMARgexWO/bTouJbt7IE
IlKVgJNp6I5MZfGRAy1wdALqi2cVKWlSArvX31BqVUa/oKMoYX9w0MOiqiwhqkfO
KJwGRXa/ghgntNWutMtQ5mv0TIZxMOmm3xaG4Nj/QN370EKIf6MzOi5cHkERgWPO
GHFrK+ymircxXDpqR+DDeVnWIBqv8mqYqnK8V0rSS527EPywTEHl7R09XiidnMy/
s1Hap0flhFMCAwEAAaOB9DCB8TAfBgNVHSMEGDAWgBStvZh6NLQm9/rEJlTvA73g
JMtUGjAdBgNVHQ4EFgQUu69+Aj36pvE8hI6t7jiY7NkyMtQwDgYDVR0PAQH/BAQD
AgGGMA8GA1UdEwEB/wQFMAMBAf8wEQYDVR0gBAowCDAGBgRVHSAAMEQGA1UdHwQ9
MDswOaA3oDWGM2h0dHA6Ly9jcmwudXNlcnRydXN0LmNvbS9BZGRUcnVzdEV4dGVy
bmFsQ0FSb290LmNybDA1BggrBgEFBQcBAQQpMCcwJQYIKwYBBQUHMAGGGWh0dHA6
Ly9vY3NwLnVzZXJ0cnVzdC5jb20wDQYJKoZIhvcNAQEMBQADggEBAGS/g/FfmoXQ
zbihKVcN6Fr30ek+8nYEbvFScLsePP9NDXRqzIGCJdPDoCpdTPW6i6FtxFQJdcfj
Jw5dhHk3QBN39bSsHNA7qxcS1u80GH4r6XnTq1dFDK8o+tDb5VCViLvfhVdpfZLY
Uspzgb8c8+a4bmYRBbMelC1/kZWSWfFMzqORcUx8Rww7Cxn2obFshj5cqsQugsv5
B5a6SE2Q8pTIqXOi6wZ7I53eovNNVZ96YUWYGGjHXkBrI/V5eu+MtWuLt29G9Hvx
PUsE2JOAWVrgQSQdso8VYFhH2+9uRv0V9dlfmrPb2LjkQLPNlzmuhbsdjrzch5vR
pu/xO28QOG8=
-----END CERTIFICATE-----
ckim-mbp:temp ckim$ 

ckim-mbp:temp ckim$ openssl x509 -in c -text
Certificate:
    Data:
        Version: 3 (0x2)
        Serial Number: 1 (0x1)
        Signature Algorithm: sha1WithRSAEncryption
        Issuer: C=SE, O=AddTrust AB, OU=AddTrust External TTP Network, CN=AddTrust External CA Root
        Validity
            Not Before: May 30 10:48:38 2000 GMT
            Not After : May 30 10:48:38 2020 GMT
        Subject: C=SE, O=AddTrust AB, OU=AddTrust External TTP Network, CN=AddTrust External CA Root
        Subject Public Key Info:
            Public Key Algorithm: rsaEncryption
            RSA Public Key: (2048 bit)
                Modulus (2048 bit):
                    00:b7:f7:1a:33:e6:f2:00:04:2d:39:e0:4e:5b:ed:
                    1f:bc:6c:0f:cd:b5:fa:23:b6:ce:de:9b:11:33:97:
                    a4:29:4c:7d:93:9f:bd:4a:bc:93:ed:03:1a:e3:8f:
                    cf:e5:6d:50:5a:d6:97:29:94:5a:80:b0:49:7a:db:
                    2e:95:fd:b8:ca:bf:37:38:2d:1e:3e:91:41:ad:70:
                    56:c7:f0:4f:3f:e8:32:9e:74:ca:c8:90:54:e9:c6:
                    5f:0f:78:9d:9a:40:3c:0e:ac:61:aa:5e:14:8f:9e:
                    87:a1:6a:50:dc:d7:9a:4e:af:05:b3:a6:71:94:9c:
                    71:b3:50:60:0a:c7:13:9d:38:07:86:02:a8:e9:a8:
                    69:26:18:90:ab:4c:b0:4f:23:ab:3a:4f:84:d8:df:
                    ce:9f:e1:69:6f:bb:d7:42:d7:6b:44:e4:c7:ad:ee:
                    6d:41:5f:72:5a:71:08:37:b3:79:65:a4:59:a0:94:
                    37:f7:00:2f:0d:c2:92:72:da:d0:38:72:db:14:a8:
                    45:c4:5d:2a:7d:b7:b4:d6:c4:ee:ac:cd:13:44:b7:
                    c9:2b:dd:43:00:25:fa:61:b9:69:6a:58:23:11:b7:
                    a7:33:8f:56:75:59:f5:cd:29:d7:46:b7:0a:2b:65:
                    b6:d3:42:6f:15:b2:b8:7b:fb:ef:e9:5d:53:d5:34:
                    5a:27
                Exponent: 65537 (0x10001)
        X509v3 extensions:
            X509v3 Subject Key Identifier: 
                AD:BD:98:7A:34:B4:26:F7:FA:C4:26:54:EF:03:BD:E0:24:CB:54:1A
            X509v3 Key Usage: 
                Certificate Sign, CRL Sign
            X509v3 Basic Constraints: critical
                CA:TRUE
            X509v3 Authority Key Identifier: 
                keyid:AD:BD:98:7A:34:B4:26:F7:FA:C4:26:54:EF:03:BD:E0:24:CB:54:1A
                DirName:/C=SE/O=AddTrust AB/OU=AddTrust External TTP Network/CN=AddTrust External CA Root
                serial:01

    Signature Algorithm: sha1WithRSAEncryption
        b0:9b:e0:85:25:c2:d6:23:e2:0f:96:06:92:9d:41:98:9c:d9:
        84:79:81:d9:1e:5b:14:07:23:36:65:8f:b0:d8:77:bb:ac:41:
        6c:47:60:83:51:b0:f9:32:3d:e7:fc:f6:26:13:c7:80:16:a5:
        bf:5a:fc:87:cf:78:79:89:21:9a:e2:4c:07:0a:86:35:bc:f2:
        de:51:c4:d2:96:b7:dc:7e:4e:ee:70:fd:1c:39:eb:0c:02:51:
        14:2d:8e:bd:16:e0:c1:df:46:75:e7:24:ad:ec:f4:42:b4:85:
        93:70:10:67:ba:9d:06:35:4a:18:d3:2b:7a:cc:51:42:a1:7a:
        63:d1:e6:bb:a1:c5:2b:c2:36:be:13:0d:e6:bd:63:7e:79:7b:
        a7:09:0d:40:ab:6a:dd:8f:8a:c3:f6:f6:8c:1a:42:05:51:d4:
        45:f5:9f:a7:62:21:68:15:20:43:3c:99:e7:7c:bd:24:d8:a9:
        91:17:73:88:3f:56:1b:31:38:18:b4:71:0f:9a:cd:c8:0e:9e:
        8e:2e:1b:e1:8c:98:83:cb:1f:31:f1:44:4c:c6:04:73:49:76:
        60:0f:c7:f8:bd:17:80:6b:2e:e9:cc:4c:0e:5a:9a:79:0f:20:
        0a:2e:d5:9e:63:26:1e:55:92:94:d8:82:17:5a:7b:d0:bc:c7:
        8f:4e:86:04
        
```
