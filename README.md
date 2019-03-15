# HS5 Binaries

## Data flow

```
Apps(socks5) <---------------+
                             |
                             v
Apps(tproxy) <--> HS5T <--> HS5C <--> [Remote HS5S]
```

## HS5C
Socks5 client - Provide socks5 service

```bash
./hs5c hs5c.conf
```

## HS5T
Socks5 transparent proxy - Redirect TCP and DNS via socks5

```bash
./hs5t hs5t.conf
```

## HTP
Transparent proxy prefix script - Control which apps via socks5

```bash
htp wget http://...
htp git clone git://...
```
