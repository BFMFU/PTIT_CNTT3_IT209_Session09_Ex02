root@azvps-dynamic:~# docker run -d -p 8080:80 --name my-web nginx:alpine       60e8ad987020eb23efd4887e5446d6d6c040f2e2d7114afa8dcf81e6c3e7da86
root@azvps-dynamic:~# docker ps
CONTAINER ID   IMAGE          COMMAND                  CREATED         STATUS         PORTS                                     NAMES
60e8ad987020   nginx:alpine   "/docker-entrypoint.…"   8 seconds ago   Up 7 seconds   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   my-web
9a2294b0716c   nginx:alpine   "/docker-entrypoint.…"   2 hours ago     Up 2 hours                                               ex5-web-1
root@azvps-dynamic:~# curl http://localhost:8080
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
html { color-scheme: light dark; }
body { width: 35em; margin: 0 auto;
font-family: Tahoma, Verdana, Arial, sans-serif; }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, nginx is successfully installed and working.
Further configuration is required for the web server, reverse proxy,
API gateway, load balancer, content cache, or other features.</p>

<p>For online documentation and support please refer to
<a href="https://nginx.org/">nginx.org</a>.<br/>
To engage with the community please visit
<a href="https://community.nginx.org/">community.nginx.org</a>.<br/>
For enterprise grade support, professional services, additional
security features and capabilities please refer to
<a href="https://f5.com/nginx">f5.com/nginx</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
root@azvps-dynamic:~# docker stop my-web
docker rm my-web
my-web
my-web
root@azvps-dynamic:~# docker stop ex5-web-1
ex5-web-1
root@azvps-dynamic:~# docker rm ex5-web-1
ex5-web-1
root@azvps-dynamic:~# docker ps -a
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES
root@azvps-dynamic:~#
