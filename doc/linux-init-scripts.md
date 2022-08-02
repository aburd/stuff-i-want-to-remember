## Description

### crontab -e with @reboot keyword

You can tell a script to run at startup using crontab

First create some script then register with `crontab -e`. 
Most versions of crontab support using the `@reboot` keyword in place of the
normal time values.

```
@reboot sh /home/user/my-script.sh
```

### update-rc.d

You can make run an init script at boot for linux adding a script to `/etc/init.d` and registering it with the `update-rc.d` command.

```
sudo update-rc.d minidlna defaults
```

This should add the service to the automatic startup system. But if you get:

```
System start/stop links for /etc/init.d/minidlna already exist.
```

Do the command

```
sudo update-rc.d minidlna enable
```

## More Info

- [AskUbuntu
  Thread](https://askubuntu.com/questions/9382/how-can-i-configure-a-service-to-run-at-startup)

## Tags

- linux
- ubuntu
- boot
- start up
- init.d
- update-rc.d
