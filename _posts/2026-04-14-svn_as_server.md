---
layout: post
title: "Установка SVN сервера как службы"
date: 2026-04-14 10:00:00 +0300
categories: [разное]
---

# Установка SVN сервера как службы

Для установки сервера [[SVN]] в системе выполняем следующий bat-файл:
```
@echo off
sc create svnserve binpath= "\"C:\Program Files\TortoiseSVN\bin\svnserve.exe\" --service --root D:\SVN\work --listen-host 0.0.0.0" displayname= "Subversion" depend= tcpip start= auto
sc description svnserve "Server Subversion (svnserve)"
```
