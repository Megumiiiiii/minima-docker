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

## Run
```
docker run -d -e minima_mdspassword=123 -e minima_server=true -v ~/minimadocker9001:/home/minima/data -p 9001-9004:9001-9004 --restart unless-stopped --name minima9001 minimaglobal/minima:latest
```

## Auto update
```
docker run -d --restart unless-stopped --name watchtower -e WATCHTOWER_CLEANUP=true -e WATCHTOWER_TIMEOUT=60s -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower
```

## Open mini DApp
`https://YourServerIP:9003/`
![Screenshot_22](https://user-images.githubusercontent.com/98658943/201584409-8f12e95a-c261-4041-ac0d-e513cbdb0aa1.png)
Enter password : 123
Login

### Incentive programs
![download](https://user-images.githubusercontent.com/98658943/201584579-528ee874-1de2-41a6-8d9f-643f3908d43e.png)
Paste Incentive ID from [HERE](https://incentive.minima.global/account/register?inviteCode=BLEVICKP)

### Check Logs
```
docker logs -f minima9001
```

