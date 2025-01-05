- Requisiti Base

sudo apt install docker-compose                 Installa docker compose

- File docker-compose.yml

version: '3'
services:
  homeassistant:
    container_name: homeassistant
    image: ghcr.io/home-assistant/home-assistant:stable
    # Mantieni l'host network per far funzionare correttamente il discovery e i protocolli di broadcast
    network_mode: host
    # privileged: true consente l'accesso ai dispositivi hardware
    privileged: true
    restart: unless-stopped
    volumes:
      - ./config:/config
    devices:
      - /dev/ttyAMA0:/dev/ttyAMA0
    volumes:
      - /var/run/dbus:/var/run/dbus
    # Impostiamo la variabile d'ambiente necessaria a Home Assistant per trovare il DBus
    environment:
      - DBUS_SYSTEM_BUS_ADDRESS=unix:path=/var/run/dbus/system_bus_socket

- Gestione Home Assistant

docker-compose up -d                            Run di home assistant
docker-compose stop                             Stop di home assistant
docker-compose down                             Stoppa e rimuovi il container

http://192.168.1.5:8123/                        Url di accesso in locale