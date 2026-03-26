# MediaNet Docker Stack

## 1) Create required folders (Linux)

Run this from the project root:

```bash
mkdir -p config/{prowlarr,sonarr,radarr,bazarr,qbit,jellyfin,jellyseerr} data/{downloads,media/{movies,tv,yt}}
```

## 2) Create your env file

```bash
cp .env.example .env
```

Then edit `.env` and set your VPN credentials (`OPENVPN_USER`, `OPENVPN_PASSWORD`) and any other values you want to customize.

## 3) Start the stack

```bash
docker compose --env-file .env -f docker-compose.medianet.yaml up -d
```

## 4) Stop the stack

```bash
docker compose --env-file .env -f docker-compose.medianet.yaml down
```
