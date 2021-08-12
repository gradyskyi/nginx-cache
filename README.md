Docker cache
===============================

### Run docker-compose

```
docker-compose up -d
```

### Install luarocks and md5 module
```
docker exec -it nginx-cache_web_1 sh

wget https://luarocks.org/releases/luarocks-3.7.0.tar.gz
tar zxpf luarocks-3.7.0.tar.gz
cd luarocks-3.7.0
./configure && make && sudo make install

luarocks install md5
```

### Open image url:

http://localhost:8080/images/image-01.png

### Trying to clear single cache file:

```
curl -X PURGE http://localhost:8080/images/image-01.png
```


