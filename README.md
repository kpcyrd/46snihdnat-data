# 46snihdnat-data

This repo contains zone information for `hamburgmesh.net`. This repo is automatically pulled every 15min, create a pull request to get a subdomain. The proxy is limited to `2001:bf7::/32` and `2a03:2267::/32`, so you need an ipv6 address from one of those ranges.

## Get a subdomain

```
# point an A record to the proxy
yoursub         A       $SNI
# point an AAAA record to your server
yoursub         AAAA    2001:bf7::1
# point an AAAA record to your server, create an A record to the proxy, all-in-one
yourothersub    %       2001:bf7::2
```

## Use your own domain

1. Register a domain
2. Create an AAAA record pointing to your server
   (Needs to be located in `2001:bf7::/32` or `2a03:2267::/32`)
3. Create an A record pointing to `46.101.199.212`

## Powered by

[kpcyrd/46snihdnat](https://github.com/kpcyrd/46snihdnat)
