# Termux

## Backup
```
tar -zcf /sdcard/termux-backup.tar.gz -C /data/data/com.termux/files ./home ./usr
```

## Restore
```
tar -zxf /sdcard/termux-backup.tar.gz -C /data/data/com.termux/files --recursive-unlink --preserve-permissions
```

## NetHunter Installer
```
wget -O install-nethunter-termux https://offs.ec/2MceZWr
```
```
chmod +x chmod +x install-nethunter-termux
```
```
./install-nethunter-termux
```