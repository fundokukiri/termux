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

## Split
```
split -b 50M -d termux-backup.tar.gz termux-backup.tar.gz.part
```

## Merge
```
cat termux-backup.tar.gz.part* > termux-backup.tar.gz
```