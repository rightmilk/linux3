# 0309 第四週筆記
## docker介紹
### aufs
系統有任何的更動會多形成一層，每一層只記錄跟下一層的差異
### 運行docker
```
# docker images  ##查看可用docker映像檔
# docker run -it ubuntu bash
##若在docker啟動時新增檔案，未保存直接退出，檔案將會喪失

##若要保存
root@jfiwohfu2j0f:/# (ctrl+p ctrl+q)  ##docker仍存在只是先跳出
# docker ps  ##查看運行中的docker
# docker commit jfi ubuntu:v1
# docker attach jfi  ##回到docker原terminal
##若要開啟新的terminal
# docker exec -it jfi sh
```

### busybox(可執行ping, ifconfig)
```
# docker pull busybox
# docker run -it busybox sh
```

### 開啟網頁伺服器
```
# docker run -d -p 8888:80 httpd  ##localport:dockerport
docker# ifconfig
##可嘗試在本地端開啟127.0.0.1:8888
```