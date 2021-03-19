### Reference
 - https://lynlab.co.kr/blog/72
 
### open port 80, 443 (port forwarding to dev)
 - port forwarding on NAT
 - firewall-cmd

### run certbot with standalone
 - mkdir /etc/letsencrypt
 - docker run -it --rm -v '/etc/letsencrypt:/etc/letsencrypt' -p 80:80 -p 443:443 certbot/certbot certonly -d 'dev.comcall.co.kr' --standalone
 - docker run -it --rm --name certbot -v '/etc/letsencrypt:/etc/letsencrypt' -v '/var/lib/letsencrypt:/var/lib/letsencrypt' certbot/certbot certonly -d 'madang.io,*.madang.io' --manual --server https://acme-v02.api.letsencrypt.org/directory
 

