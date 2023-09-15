# Snippets
Collection of commands, one liners



## Start HTTP static file server

- Using Caddy webserver `caddy file-server --browse :80`
- Using Python3 `python -m http.server 80`


## Get IP address

- cmd: `ipconfig`
- powershell: `Get-NetIPAddress -AddressFamily IPV4` 
- bash: `ifconfig` or `hostname -I` or `ip a`

## Renew Let's Encrypt SSL certificate

```bash
sudo snap install --classic certbot
sudo ln -s /snap/bin/certbot /usr/bin/certbot
sudo snap set certbot trust-plugin-with-root=ok
sudo certbot certonly --manual --preferred-challenges dns -d example.com -d *.example.com
```
