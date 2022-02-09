# nextkast-remote-service
A Simple Binary Service that runs on Windows Mac and Linux it can get simply downloaded and started from any folder you need to register the service your self via your operating system.


## Configuration
by default this service will execute what ever config.js is next near to it in the same folder.
a example configuration for nextKast BX looks like

Use this
```js
const selfSignedCert = {
    key: '-----BEGIN PRIVATE KEY-----\nMIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQDN+ctDLwQdqXJu5z4ZJU8PRdl2p/MbSplYOOa7pZ7fUuQAdYUXI2uC0DXsN9KhLF/bvS6CpPMc4v6l3yPPrbUaMnYKR1zf/EG8JXYViGKLDGR/kUtIy5DAG6ps25l+oU+EkpEbWKDwGFXrXPpizyea0yNqts3QJJFz/52RE553VWrOuYe73WpGIjTVZYJAs4NaQmaW4rAI9Rwlx72+j+TXPTGJ6AW+WNFaDgNmJ8yVeEhehMWmKHky0hWFrrK8kRqTjVYiZQ0jtEeg0tBXAy5uGa69PZUcdXwFNuHpo3n+B8UceIiUwmdIFDLJUHh0Pw7B0Kyhx9xtVbZ2P1kja/Q9AgMBAAECggEAWbeOQ8s83baq84eh0s4fa6WfHUH2cFLEDFtslRuE4f129oQ53mQ9NhN/CU8fXbi4YDw9AAbdJh3xkUpqjNE66xhDtiJzX9S+xTcEAkkPs0VImRAuXJzehe8HArd8Wl3lBvfYYLLwFuRiuEwde+CDfbqt2JObfigPexlCBqknAw7XZOxqaVwKxqqzS7AwdzAPvt5JMZ2LWJ5uAewA3FNtRCQqwzneYPw8nC90J6krFRx5Qk4AnZpNe2o1S/7FfJq5Rs3bUwDyd6YvzDfzOc/FN7sO1uV5qljuvXDh0+4uzdYPmwAiXtdbzdLFpW930lC+kOfiHURbPjMGfu28/y+DuQKBgQDv6FvHh8kclRA3st0bk1GXbTZax6LvMeR8fO61aq/OY+E0DYfhCXrjnnDlU4cBjZ/LA7amnYa718hN06thqlCnheqSWum7zJc4WdL81u1zzfKUbt82FQ0jNzzSpDtMHwzUDh62fZBtINZ5i4u1+jeHkKsaPaJ9R30lfh0LQ2GNtwKBgQDbysO0a+ju4DXuzPJv5uX+X6zuYKY2ewma50PMXWD6q/PPXCgrNajXgaTmDHttAgClHJwgHQjhMbdt/uv3/SzUG+cU6e8rvby7B0sEyl3gS6wAzTV9d8VjkBVLAi7QOiiu70CSjXw+g7tQ41NSRW+jcbrqW1XP6AAXRjBwO3ANqwKBgQC4FiPWx2qadActtiHTtwc0mqjKn8V2pWId4/+HVYXxaNK1jmxlUVDqt/kI/z7pAjNLJF5TGyz3lmwsy+8F0hpxcWC9TOVtJWAj7UjomkM6SR2KqEi+xwh9rTUOrNaTYoAFd5A5l7/q/PeV7G4YBRf2/htM116HowN0cYD304xXoQKBgEMAGoyDYKyA+K/lFfp6vp2+eK7qE4EEHLd1zDseNBP2GwqZIz2Yy/F1+diO8YkXVS7/+6/mafCMAUisry4XpXS7VMQRU/FXk5LH9FxvfBKFvtc3txiaTDe/kl4dOjwLnp9FG8ARFVDRQ2azBZFMzW1bnAkY8p3AMVbm9Jkh5VSlAoGAWMLLRcWWxvG61YnSvjpdwTbi+nAmfNz+N81uMjTqFON/8YYEuuVC7jGjgTpyv4mWIbU+1MQW8U10rnQCvrCA0k1QCam9zrP5S4gNX6rqzNRm3zDfGGSYoqRMEK+0j6AIgAvV9DJ0rPcz7GA5aFM3ia9oUdmLdf90TPAEy7D75SM=\n-----END PRIVATE KEY-----',
    cert: '-----BEGIN CERTIFICATE-----\nMIIDkzCCAnugAwIBAgIUaxuZYwNCdBsOL8DbYC5vxBnTA3cwDQYJKoZIhvcNAQELBQAwWTELMAkGA1UEBhMCQVUxEzARBgNVBAgMClNvbWUtU3RhdGUxITAfBgNVBAoMGEludGVybmV0IFdpZGdpdHMgUHR5IEx0ZDESMBAGA1UEAwwJbG9jYWxob3N0MB4XDTIxMTEyODA4MjkyMVoXDTIxMTIyODA4MjkyMVowWTELMAkGA1UEBhMCQVUxEzARBgNVBAgMClNvbWUtU3RhdGUxITAfBgNVBAoMGEludGVybmV0IFdpZGdpdHMgUHR5IEx0ZDESMBAGA1UEAwwJbG9jYWxob3N0MIIBIjANBgkqhkiG9w0BAQEFAAOCAQ8AMIIBCgKCAQEAzfnLQy8EHalybuc+GSVPD0XZdqfzG0qZWDjmu6We31LkAHWFFyNrgtA17DfSoSxf270ugqTzHOL+pd8jz621GjJ2Ckdc3/xBvCV2FYhiiwxkf5FLSMuQwBuqbNuZfqFPhJKRG1ig8BhV61z6Ys8nmtMjarbN0CSRc/+dkROed1VqzrmHu91qRiI01WWCQLODWkJmluKwCPUcJce9vo/k1z0xiegFvljRWg4DZifMlXhIXoTFpih5MtIVha6yvJEak41WImUNI7RHoNLQVwMubhmuvT2VHHV8BTbh6aN5/gfFHHiIlMJnSBQyyVB4dD8OwdCsocfcbVW2dj9ZI2v0PQIDAQABo1MwUTAdBgNVHQ4EFgQUH9an2MwjoZAeKtz/x0UkfSrFRfAwHwYDVR0jBBgwFoAUH9an2MwjoZAeKtz/x0UkfSrFRfAwDwYDVR0TAQH/BAUwAwEB/zANBgkqhkiG9w0BAQsFAAOCAQEAm5v8kansSPF/uA5LBqMrNgKgwUdez/AKOgWP8CRVqEomhGc+U6gr0p0gTtNZB73Vtc0Zvag/t0jqRtAJFE61FkCiiouMUw3lGY/NyFLe975eyOo5ay/rNCXUckN29mP+wVdOx6Mo/roK6lxrOts5r5O0F24xwiXqQiXE8JdbGDQ16jst178eUfH74jaItWu74a3kxHMg2qohWg1/gWCjv+okSZ2oaN7IEnxsHQUo6Owurc4EYpw6j5BZXSP4SYVZZLym3COA1qnRtn8eHFrl3GocOz6fohWwK8qC9mZU9FlmCOIe+vInNDuG0yQtk/vskjbop3EetNvCAsr0ubabVQ==\n-----END CERTIFICATE-----',
}
```

or read from the file system most best same directory as the exe of the service to avoid path complications

```js
const certFiles = {
     key: fs.readFileSync('valid-ssl-key.pem', 'utf8'),
     cert: fs.readFileSync('valid-ssl-cert.pem', 'utf8')
}
```

step 3. after that configure the Proxy for nextKast BX
```js
const proxyServer = httpProxy.createServer({
    target: { 
        host: 'localhost', 
        port: 9009 
    },
    ssl: selfSignedCert, // or use certFiles here depending on what u did choose
    ws: true,
    secure: false,
})
```

step 4. listen on a port skip that step if you plan to use LiveMic

```js
proxyServer.listen(8009);
```


Thats all needed to replace Nginx in nextKast BX

## Advanced Configuration Including liveMic Support

everything before applys but you skip step 4
```js
const httpRouter = HttpRouter();
httpRouter.get('/favicon.ico', (req) => req.res?.status(204).end()); // Disable favicon

httpRouter.use('/', (req) => proxyServer.web(req, req?.res)); // Will serve everything that is returned by nextKast MobileVT

// Single Page Apps are also supported please ask the support about that.
const httpsServer = createSecureServer(selfSignedCert, httpRouter); // use certFiles if u used that before exposes https://
const webSocketServer = new WebSocketServer(httpsServer); // exposes wss://

// Creates a Bidirectional unfiltered Channel Between all users of the wss://<host:port>/livemic url 
httpRouter.use('/livemic',HttpRouter.static('./public/livemic')); // Will serve everything that is in the public subfolder of this service. Or what is packed with the service
const liveMic = webSocketServer.of('/livemic'); 
liveMic.on('connect',  (/** @type {Socket} */ stream) => {
    stream.on('message', (data) => {
        console.log(`${stream.id}:message: `, data);
        stream.broadcast.emit('message', data); 
    });
});

```



after that the main configuration is done install now the nextkast pwa 
https://nextkast.com/install-remote-interface


## Optional Advanced Auto Update Capabilities.
Configure your nextKast Remote interface give it write permissions to the folder where you did put the files for the service.


