# docker-image-wrapper

```
for i in $(cat imagelist);do
    echo $i
    dirname=$(basename $i | awk -F':' '{print $1}')
    mkdir -p $dirname
    echo FROM $i > $dirname/Dockerfile
    echo MAINTAINER ikubernetes 1347054988@qq.com >> $dirname/Dockerfile
done
```