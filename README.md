HTTPS 2048-bit RSA TLS/SSL Cert Example
====

This is targeted towards people who are using io.js / node.js,
but as far as generating and testing certs, these are the exact
same **openssl** commands you'd use with any language.


Here's the zero-config example:

```
git clone https://github.com/coolaj86/nodejs-ssl-example.git

pushd nodejs-ssl-example

npm install
node ./serve.js
```

Then visit <https://local.helloworld3000.com:8043>.

**Note**: Your browser will warn you that you the server is using a bogus
certificate authority. That's okay for the purposes of this example.

Special Notes
----

The key to this example is that **the certs are not self-signed**.
Using self-signed certs is the stupidest thing that anyone ever tried to do in a browser.

Instead, a bogus Root CA is created. Then the bogus Root CA is used to sign the certificates.

If only the world knew that all you have to do to fix Self-Signed Certificate errors
is to create one additional certificate and use that as the Certificate Authority...

Full Article
-----

See the full article at
[How to create a Certificate Signing Request (CSR) for HTTPS (TLS/SSL) RSA PEMs](http://blog.coolaj86.com/articles/how-to-create-a-csr-for-https-tls-ssl-rsa-pems/)

Other SSL Resources
=========

Zero-Config clone 'n' run (tm) Repos:


* [io.js / node.js HTTPS SSL Example](https://github.com/coolaj86/nodejs-ssl-example)
* [io.js / node.js HTTPS SSL Self-Signed Certificate Example](https://github.com/coolaj86/nodejs-self-signed-certificate-example)
* [io.js / node.js HTTPS SSL Trusted Peer Client Certificate Example](https://github.com/coolaj86/nodejs-ssl-trusted-peer-example)
* [SSL Root CAs](https://github.com/coolaj86/node-ssl-root-cas)

Articles

* [http://greengeckodesign.com/blog/2013/06/15/creating-an-ssl-certificate-for-node-dot-js/](Creating an SSL Certificate for node.js)
* [http://www.hacksparrow.com/express-js-https-server-client-example.html/comment-page-1](HTTPS Trusted Peer Example)
* [How to Create a CSR for HTTPS SSL (demo with name.com, node.js)](http://blog.coolaj86.com/articles/how-to-create-a-csr-for-https-tls-ssl-rsa-pems/)
* [coolaj86/Painless-Self-Signed-Certificates-in-node](https://github.com/coolaj86/node-ssl-root-cas/wiki/Painless-Self-Signed-Certificates-in-node.js)
