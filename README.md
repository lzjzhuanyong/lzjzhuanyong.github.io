# lzjzhuanyong.github.io
signature tool for work

[index.html](https://lzjzhuanyong.github.io) back to the basic index page

~~index.html~~ [signingTool.html](https://lzjzhuanyong.github.io/signingTool.html) uses [forge.js](https://github.com/digitalbazaar/forge) as the module to sign the query string by using the HMAC SHA256 algorithm. 

~~[wstool.html](https://lzjzhuanyong.github.io/wstool.html) uses [pako.js](https://github.com/nodeca/pako) as the module to decompress the gzip data.~~

[wstool.html](https://lzjzhuanyong.github.io/wstool.html) no longer uses "pako.js" to do decompression

2022-10-14 update: new page style of the wstool

2022-10-20 update: datalist of input label for url quick choosing, and add new optional functions for more composability

2023-01-06 update: Add a new page for the RSA key generation tool, [rsaGenerator.html](https://lzjzhuanyong.github.io/rsaGenerator.html).  This page is fully designed with friendly style. 
(I was manually added the web worker script for the RSA generation, not used the forge.js imbedded web worker function, because I want to learn and familiar with this feature.)

2023-01-09 update: Re-designed the style of the signature tool, [signingTool.html](https://lzjzhuanyong.github.io/signingTool.html), and support signing the query string to get signature with the RSA format key.

2023-01-10 update: Add a new tool for timestamp format conversion.

2023-05-07 update: Create a new tool to test websocket api, [wsapitool.html](https://lzjzhuanyong.github.io/wsapitool.html). And add a back home page box button for all tools.

2023-05-11 update: Create a pay signature tool [paysigningtool.html](https://lzjzhuanyong.github.io/paysigningtool.html). The pay signature algorithm is HMAC SHA512, it is different from the public endpoint signature method(HMAC SHA256/RSASSA-PKCS1-v1.5). And the main change of this tool is aborting import an external encrypt library like the forge.js that used by previous tools, and only use the browser built in web api interfaces, subtle crypto method to sign the data.

2023-05-12 update: Add a new style to hide the secret key and private key on the page for signature tool [signingTool.html](https://lzjzhuanyong.github.io/signingTool.html)

2023-05-13 update: websocket api test tool supports rsa key, fix some bugs

2023-05-15 update: new feature of key generator to support generating ed25519 key. new feature of signature tool to support ed25519 key to sign request. New feature of websocket api tool to support ed25519 key to sign request. ED25519 key uses the latest forge.js to generate, due to the forge.js only generate the raw key(binary format), the pem format display should be done by the self coded function. To be consistent with the format generated by openssl, referred the article of [ASN.1 and DER](https://letsencrypt.org/docs/a-warm-welcome-to-asn1-and-der/) and [RFC8410](https://www.rfc-editor.org/rfc/rfc8410)

2023-05-16 update: ed25519 private key pem meets the openssl and PyCryptodome style. Note: the spot testnet doesn't supported the URL encoded query string of ed25519 signature, but could get through without url encoded signature. Test with request body or websocket api tool

2023-06-13 update: fixed a bug in the wsapitool

2023-08-27 update: add a new tool for html transcoding
