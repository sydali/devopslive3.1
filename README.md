# devopslive3.1

## App output and image
```


root@dice-devops:/home/Repos/devopslive3.1# docker build -t my-python-app .
[+] Building 6.2s (9/9) FINISHED                                                                                                                                                                                                               docker:default
 => [internal] load build definition from Dockerfile                                                                                                                                                                                                     0.0s
 => => transferring dockerfile: 532B                                                                                                                                                                                                                     0.0s
 => [internal] load .dockerignore                                                                                                                                                                                                                        0.0s
 => => transferring context: 2B                                                                                                                                                                                                                          0.0s
 => [internal] load metadata for docker.io/library/python:latest                                                                                                                                                                                         0.7s
 => [1/4] FROM docker.io/library/python@sha256:41d8a0a357debbd80cdc257b2c08d272984a0e536ff69a01a8b939ab0a6ccc12                                                                                                                                          0.0s
 => [internal] load build context                                                                                                                                                                                                                        0.0s
 => => transferring context: 2.47kB                                                                                                                                                                                                                      0.0s
 => CACHED [2/4] WORKDIR /app                                                                                                                                                                                                                            0.0s
 => [3/4] ADD . /app                                                                                                                                                                                                                                     0.0s
 => [4/4] RUN pip install -r requirements.txt                                                                                                                                                                                                            5.1s
 => exporting to image                                                                                                                                                                                                                                   0.3s
 => => exporting layers                                                                                                                                                                                                                                  0.3s
 => => writing image sha256:4c75a4c3652ade10a9054944cdebf37b2703b308a0b217eef0b63e47ca8ee7c8                                                                                                                                                             0.0s
 => => naming to docker.io/library/my-python-app                                                                                                                                                                                                         0.0s
root@dice-devops:/home/Repos/devopslive3.1# docker images
REPOSITORY                         TAG             IMAGE ID       CREATED              SIZE
my-python-app                      latest          4c75a4c3652a   3 seconds ago        1.03GB
<none>                             <none>          379664886057   About a minute ago   1.03GB
devopslive22_web                   latest          80153877045c   5 days ago           214MB
prom/prometheus                    latest          620d5e2a39df   5 days ago           247MB
jenkins/jenkins                    latest          d8dd2fa90f20   7 days ago           476MB
grafana/grafana                    latest          a00c0638216f   7 days ago           399MB
prom/node-exporter                 latest          72c9c2088986   8 days ago           22.7MB
quay.io/prometheus/node-exporter   latest          72c9c2088986   8 days ago           22.7MB
redis                              alpine          246a9110fd9e   11 days ago          43.4MB
postgres                           13              d28d5ae8775c   11 days ago          413MB
unicorn                            v1              94d5dc12ddea   12 days ago          1.04GB
rollymaan/assignmet-1              v1              94d5dc12ddea   12 days ago          1.04GB
kicbase/stable                     v0.0.42         dbc648475405   2 weeks ago          1.2GB
apache/airflow                     2.7.3           56d2fbb018bb   2 weeks ago          1.54GB
redis                              latest          7f27d60cb8e0   2 weeks ago          138MB
nginx                              latest          c20060033e06   2 weeks ago          187MB
httpd                              latest          7f6a969e81a5   2 weeks ago          168MB
debian                             bullseye-slim   8546b63bb8a1   2 weeks ago          80.6MB
alpine                             latest          8ca4688f4f35   7 weeks ago          7.34MB
centos                             latest          5d0da3dc9764   2 years ago          231MB
gcr.io/cadvisor/cadvisor           latest          68c29634fe49   2 years ago          163MB
google/cadvisor                    latest          eb1210707573   5 years ago          69.6MB
root@dice-devops:/home/Repos/devopslive3.1# docker run -ti -p 3040:3040  my-python-app
 * Serving Flask app 'app'
 * Debug mode: off
WARNING: This is a development server. Do not use it in a production deployment. Use a production WSGI server instead.
 * Running on all addresses (0.0.0.0)
 * Running on http://127.0.0.1:3040
 * Running on http://172.17.0.3:3040
Press CTRL+C to quit
103.85.36.175 - - [21/Nov/2023 16:42:04] "GET / HTTP/1.1" 200 -
103.85.36.175 - - [21/Nov/2023 16:42:04] "GET /favicon.ico HTTP/1.1" 404 -
^Croot@dice-devops:/home/Repos/devopslive3.1#

```



