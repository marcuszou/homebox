# HomeBox

Try-out just starts. This is a very great home inventory management app.

## Deployment with docker compose
Prepare the yaml file
```shell
services:
  homebox:
    image: ghcr.io/hay-kot/homebox:latest
    container_name: homebox
    restart: unless-stopped
    environment:
      - HBOX_WEB_MAX_UPLOAD_SIZE=10
      - TZ=America/Edmonton
    volumes:
      - ./data:/data/
    ports:
      - 3100:7745
```
Then launch the app:
```shell
docker compose up -d
```

then launch the website:
```shell
http://localhost:3100
```

## Give a try
Beautiful GUI

## License
MIT
