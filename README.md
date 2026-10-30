# Termux Backup & Restore

Hướng dẫn backup, restore và cài đặt NetHunter cho Termux.

## Backup

```bash
tar -zcf /sdcard/termux-backup.tar.gz -C /data/data/com.termux/files ./home ./usr
```

## Restore

```bash
tar -zxf /sdcard/termux-backup.tar.gz -C /data/data/com.termux/files --recursive-unlink --preserve-permissions
```

## NetHunter Installer

```bash
wget -O install-nethunter-termux https://offs.ec/2MceZWr
chmod +x install-nethunter-termux
./install-nethunter-termux
```

## Chia nhỏ file backup (Split)

```bash
split -b 50M -d termux-backup.tar.gz termux-backup.tar.gz.part
```

## Gộp file backup (Merge)

```bash
cat termux-backup.tar.gz.part* > termux-backup.tar.gz
```