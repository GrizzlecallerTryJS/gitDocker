This is some config for setup docker compose.
I use it for develop on my mac.

Raise containers:

docker-compose up -d --build

Down containers:

docker-compose down

The following lines need to be added to the hosts file:

127.0.0.1 my.example.com
127.0.0.1 pma.example.com
127.0.0.1 gitlab.example.com

Hosts file location:

- Linux, macOS : /etc/hosts
- Windows : %SystemRoot%\system32\drivers\etc\hosts