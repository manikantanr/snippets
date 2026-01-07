# Snippets
Collection of commands, one liners



## Start HTTP static file server

- Using [Caddy webserver](https://github.com/caddyserver/caddy) `caddy file-server --browse :80`
- Using Python3 `python -m http.server 80`
- Using [static-web-server](https://github.com/static-web-server/static-web-server)  `static-web-server --host 0.0.0.0 --port 8000  --directory-listing --root /opt/data`


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


## Markdown to PDF
```bash
pandoc your_file.md -o output.pdf --pdf-engine=wkhtmltopdf --toc --number-sections --pdf-engine-opt=--grayscale --pdf-engine-opt=--footer-right --pdf-engine-opt="[page]"

```

## Download youtube video
- Requires `deno` binary in path for best performance
```bash
yt-dlp --cookies-from-browser firefox -f "bestvideo+bestaudio/best" --merge-output-format mp4 "<url>"
```
