---
layout: post
title: "Сжатие базы в InterBase"
date: 2026-04-14 10:00:00 +0300
categories: [разное]
---

# Сжатие базы в InterBase

Для сжатия БД нужно сделать бэкап базы командой
```shell
gbak -b -v DataBase.gdb backup.gdb -user USER_NAME -password PASSWORD
```
И восстановить её обратно, уже без мусора
```shell
gbak -c -v backup.gdb DataBase.gdb -user USER_NAME -password PASSWORD
```
