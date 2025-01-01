### create user

## create password file
```
docker exec -it mosquitto touch /mosquitto/config/passwordfile
```

## change permission
```
docker exec -it mosquitto chmod 600 /mosquitto/config/passwordfile
```

## change owner
```
docker exec -it mosquitto chown root:root /mosquitto/config/passwordfile
```
## create user
```
docker exec -it mosquitto mosquitto_passwd -b /mosquitto/config/passwordfile [username] [password]
```