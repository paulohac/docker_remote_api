# How to start docker remote API 


/etc/systemd/system/docker.service.d/docker.conf

[Service]
ExecStart=
ExecStart=/usr/bin/dockerd -H tcp://0.0.0.0:2375 -H unix://var/run/docker.sock

Restart the docker service using systemd commands:

sudo systemctl daemon-reload
sudo systemctl restart docker
