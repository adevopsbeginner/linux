# linux
 - commands
 - step-by-steps

## journalctl
1. How to Check and Clean Up Journal Logs
- check logs
```
$ systemctl is-active systemd-journald
$ journalctl
$ journalctl --boot
$ journalctl --since "1 hour ago"
$ journalctl --since "2023-01-01" --until "2023-01-02"
$ journalctl -u sshd
$ journalctl -u sshd | grep error
$ journalctl -u sshd | grep stopped
$ journalctl -u sshd | grep topped
$ journalctl --disk-usage

```
- cleanup logs
```
$ journalctl --vacuum-time=200d
```

## Checking Disk Usage, df, du, ls -lh
```
du
df
ls
```

## find
```
find . -name "filename"
find . -name "*.txt"
find . -size +100M
find . -size -1k
find . -mtime -7
find . -mtime +30
find . -type d
find . -type f
find /var/log -name "*.log"
find . -name "*.tmp" -exec rm -f {} \;
find . -name "*.txt" -exec ls -lh {} \;
find . -perm 644
find . -perm /o=w
find . -name "*.log" -size +50M
find . -mtime -7 -user root
find . -name "*.txt" | wc -l
```













