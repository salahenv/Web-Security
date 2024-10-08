# XSS (Cross Site Scripting) attack and Content-Security-Policy
### What is XSS?
Adding malicius code in the application code.
### How attacker do?
Generally by sending malicius link or malicius code the input box of webpage. Once user click on it become victim of security attack.
### Consequences of XSS
- User Session Hijacking.
- Capturing Keystroke.
- Unauthorize Activity (Sending Unintended email, post or transaction on behalf of you).
### CSP (Content Security Policy)
- CSP help to detect and mitigate the XSS attack.
- CSP is set either in the headers of http or in the meta tag of html.
- Below are the list of CSP.

1. ```Content-Security-Policy: default-src 'self'``` All the content will come from the same origin excluding subdomain.
2. ```Content-Security-Policy: default-src 'self' example.com *.example.com``` All the content will come from example.com || subdmain.example.com || same origin
3. ```Content-Security-Policy: default-src 'self'; image-src example.com *.example.com``` Images will come from example.com || subdomain.example.com || same origin . Other than image will come from same origin.
4. ```Content-Security-Policy: default-src 'https://example.com'``` All the content will strictly come over secured TLS/SSL HTTP.
5. ```Content-Security-Policy: default-src 'self' script-src 'self' unsafe-inline nonce-nonceKey``` Inline script will be executed with ```unsafe-inline``` and the with ```nonce-nonceKey``` we can differentiate between our inline and injected one. The matched nonce inline script will get executed rest is ignored.

### Resources
https://dev.to/shostarsson/security-headers-to-use-on-your-webserver-3id5

# Click Hijacking and Iframe Security.
- In order to control the embeding of your web app into other website as a iframe is controlled by ```X-Frame-Options```.

### Below is posible values.
1. ```X-Frame-Options: DENY``` It will deny all website to embed our website into there as a IFrame.
2. ```X-Frame-Options: SAMEORIGIN``` Same origin can embed.
3. ```X-Frame-Options: ALLOWFROM origin 'example1.com example2.com'``` Same origin can embed.

# More Security Headers
### 1. X-Powered-By
### 2. Referrer-Policy
### 3. X-Content-Type-Options
### 4. X-XSS-Protection



