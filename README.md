# IP

A small nginx config that shows the visitor's ip address.

## Html format

```http
GET http://localhost:8080 HTTP/1.1
accept: text/html
```

```http
HTTP/1.1 200 OK
Server: nginx/1.27.2
Date: Tue, 22 Oct 2024 10:46:08 GMT
Content-Length: 243
Connection: close
Content-Type: text/html

<html><body style="margin: 0; padding: 0; background-color: #0f172a; display: flex; height: 100vh; width: 100vw; align-items: center; justify-content: center; font-family: system-ui;"><h1 style="color: #f3f4f6;">127.0.0.1</h1></body></html>
```

## Plain format

```http
GET http://localhost:8080 HTTP/1.1
accept: text/plain
```

```http
HTTP/1.1 200 OK
Server: nginx/1.27.2
Date: Tue, 22 Oct 2024 10:47:56 GMT
Content-Length: 12
Connection: close
Content-Type: text/plain

127.0.0.1
```

## Json format

```http
GET http://localhost:8080 HTTP/1.1
accept: application/json
```

```http
HTTP/1.1 200 OK
Server: nginx/1.27.2
Date: Tue, 22 Oct 2024 10:48:31 GMT
Content-Length: 21
Connection: close
Content-Type: application/json

{
  "ip": "127.0.0.1"
}
```
