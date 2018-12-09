# wordpress
Dockerized wordpress for Openshift and Kubernetes 


###### first of all, download the WordPress and extract it 
```bash
wget http://wordpress.org/latest.tar.gz
tar xfz latest.tar.gz
```

then you have to build the docker file 

```bash
$ docker build -t wordpress/rohammosalli .
$ docker tag wordpress/rohammosalli  registry-host:5000/blog/blog
$ docker push registry-host:5000/blog/blog
```

### How to use 
The following environment variables are also honored for configuring your WordPress instance on your cluster:

-e WORDPRESS_DB_HOST=... (defaults to the IP and port of the linked mysql container)
-e WORDPRESS_DB_USER=... (defaults to "root")
-e WORDPRESS_DB_PASSWORD=... (defaults to the value of the MYSQL_ROOT_PASSWORD environment variable from the linked mysql container)
-e WORDPRESS_DB_NAME=... (defaults to "wordpress")



then you can use the image in your Openshift Cluster or Kubernetes cluster ;)
