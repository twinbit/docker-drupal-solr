![Drocker](https://raw.githubusercontent.com/twinbit/drocker/gh-pages/img/logo.png)

# Docker drupal search api solr container

This image can be used as-is, it is based on search_api_solr solr 4.x configurations.

## Example fig configuration

```
solr:
  build: containers/solr
  hostname: solr
  ports:
    - "8983:8983"
  command: -Xmx1024m -DSTOP.PORT=8079 -DSTOP.KEY=stopkey -jar start.jar
```



An automated build for this repo is available on the [Docker Hub](https://registry.hub.docker.com/u/twinbit).

This image is intended to be used in conjuction with the other images of the drupal docker stack:

- [twinbit/docker-drupal-data](https://github.com/twinbit/docker-drupal-data)
- [twinbit/docker-drupal-cli](https://github.com/twinbit/docker-drupal-cli)
- [twinbit/docker-drupal-mailcatcher](https://github.com/twinbit/docker-drupal-mailcatcher)
- [twinbit/docker-drupal-mysql](https://github.com/twinbit/docker-drupal-mysql)
- [twinbit/docker-drupal-nginx](https://github.com/twinbit/docker-drupal-nginx)
- [twinbit/docker-drupal-solr](https://github.com/twinbit/docker-drupal-solr)
- [twinbit/docker-drupal-php](https://github.com/twinbit/docker-drupal-php)
