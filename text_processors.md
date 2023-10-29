1) Из файла /proc/meminfo выести всю информацию о HugePages (там скорее всего будет всё по нулям, это норма)
2) Из файла /proc/stat высести информацию про softirq
3) Вывести участников группы cdrom (файл /etc/group)
пример, группа floppy, участник anestesia
```
floppy:x:25:anestesia
```
группа scanner - участники saned и anestesia
```
scanner:x:117:saned,anestesia
```
4) Выпонить команду ```ip -o a``` и получить ip машины.
Например ip моей машины 192.168.0.70 (строка ```2: wlo1    inet 192.168.0.70/24 brd 192.168.0.255 scope global dynamic noprefixroute wlo1\       valid_lft 6207sec preferred_lft 6207sec```)
```
anestesia@anestesia:~$ ip -o a
1: lo    inet 127.0.0.1/8 scope host lo\       valid_lft forever preferred_lft forever
1: lo    inet6 ::1/128 scope host noprefixroute \       valid_lft forever preferred_lft forever
2: wlo1    inet 192.168.0.70/24 brd 192.168.0.255 scope global dynamic noprefixroute wlo1\       valid_lft 6207sec preferred_lft 6207sec
2: wlo1    inet6 fe80::a5b:d6ff:fe18:e8e0/64 scope link noprefixroute \       valid_lft forever preferred_lft forever
anestesia@anestesia:~$
```
