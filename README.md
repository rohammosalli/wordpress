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

the you can use the image in your Openshift Cluster or Kubernetes cluster ;)
