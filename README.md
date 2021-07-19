# simple-chat-app

Example app written for article purpose:
[How to write video chat app using webrtc and nodejs](https://tsh.io/blog/how-to-write-video-chat-app-using-webrtc-and-nodejs/)  

## creating certificate files
HTTPS connection is required to access the webrtc API from remote browser.  
```
$ openssl genrsa -out key.pem
$ openssl req -new -key key.pem -out csr.pem
$ openssl x509 -req -days 9999 -in csr.pem -signkey key.pem -out cert.pem
$ rm csr.pem
```
