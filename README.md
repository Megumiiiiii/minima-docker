# minima-docker

## Uninstall Previous services
```
sudo wget -O minima_remove.sh https://raw.githubusercontent.com/minima-global/Minima/master/scripts/minima_remove.sh && chmod +x minima_remove.sh && sudo ./minima_remove.sh -p 9001 -x
```

```
sudo rm -r /home/minima/
sudo userdel minima
```

## Add new user
```
wget -O minimad.sh https://raw.githubusercontent.com/Megumiiiiii/minima-docker/main/minimad.sh && chmod +x minimad.sh && ./minimad.sh
```

### New Password

![Screenshot_20](https://user-images.githubusercontent.com/98658943/201586116-fc14131f-c296-4b88-b45a-ef194f660394.png)

Submit new password, click Enter, Y , Enter


## Run
```
docker run -d -e minima_mdspassword=123 -e minima_server=true -v ~/minimadocker9001:/home/minima/data -p 9001-9004:9001-9004 --restart unless-stopped --name minima9001 minimaglobal/minima:latest
```

## Run Auto Updater
```
docker run -d --restart unless-stopped --name watchtower -e WATCHTOWER_CLEANUP=true -e WATCHTOWER_TIMEOUT=60s -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower
```

## Open mini DApp
`https://YourServerIP:9003/`

![Screenshot_25](https://user-images.githubusercontent.com/98658943/201585218-c98fe73a-4253-494b-a46b-1abf09a389c1.png)

If you can't open, follow [THIS GUIDE](https://www.vultr.com/docs/how-to-bypass-the-https-warning-for-self-signed-ssl-tls-certificates/)



Enter password : 123
Click Login

### Incentive programs
![download](https://user-images.githubusercontent.com/98658943/201584579-528ee874-1de2-41a6-8d9f-643f3908d43e.png)


Paste Incentive ID from [HERE](https://incentive.minima.global/account/register?inviteCode=BLEVICKP)

### Check Logs
```
docker logs -f minima9001
```

![Screenshot_21](https://user-images.githubusercontent.com/98658943/201586792-d0d1c2f1-0f91-4b7e-855e-99b44597d7e6.png)
