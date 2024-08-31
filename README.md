## forked from hwdsl2/ipsec-vpn-server and added l2tp without IPSec


# How To Use

```bash
docker run -d --privileged -p 1701:1701/udp -p 500:500/udp -p 4500:4500/udp --name l2tp --restart=always --env-file /root/docker/l2tp/vpn.env -v /lib/modules:/lib/modules:ro gritsenko/l2tp_without_ipsec:latest
```

# File vpn.env

```bash
# Define IPsec PSK, VPN username and password
VPN_IPSEC_PSK=bigass
VPN_USER=user
VPN_PASSWORD=vpnallow

# Define additional VPN users
# VPN_ADDL_USERS=additional_username_1 additional_username_2
# VPN_ADDL_PASSWORDS=additional_password_1 additional_password_2
```
