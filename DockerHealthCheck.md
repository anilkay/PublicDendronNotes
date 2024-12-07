---
id: ww78gl02vq2cmgckgoo1mj2
title: DockerHealthCheck
desc: ''
updated: 1733604798849
created: 1733604774984
---
# Docker HealthCheck

Dockerfile'a direkt olarak eklenebiliyor ve 
Container içinde çalışıyor. Bu sayede container içindeki executablelar
yardımı ile kullanabiliyoruz. 

Örnek olarak Curl ile:
```
HEALTHCHECK --interval=30s --timeout=10s --start-period=15s --retries=3 \
  CMD curl -f http://localhost:8080/Health || exit 1
```

Health metodunda ben sadece db'den bir veri çekmeyi denedim.
Eğer Db yanında cache vb ya da başka bağımlı olduğu servisler olsaydı 
hepsini kontrol etmem gerekirdi. 
