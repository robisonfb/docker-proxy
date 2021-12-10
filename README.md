# NGINX Reverse Proxy Docker


### iniciando site1
```
cd site1/
docker-compose build
docker-compose up -d
```

### iniciando site2
```
cd site2/
docker-compose build
docker-compose up -d
```

### Iniciando proxy

```
cd proxy/
docker-compose build
docker-compose up -d
```


### Configurando o hosts
```
sudo nano /etc/hosts
```
Adicionar essas rotas
```
127.0.1.1 site1.test
127.0.1.1 site2.test
```



## Criar um novo certificado SSL

```
cd proxy\ssl

sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout site1.key -out site1.crt 
```

