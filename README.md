# Wiki.js Walkthrough

## Running on local device with docker-compose

Clone the repository for docker-compose file.

```shell
git clone https://github.com/snoop2head/wiki-js-docker.git
cd ./wiki-js-docker
```

Run docker on local device && Build two separate images using docker-compose

```shell
docker-compose up --build
```

(Optional) If you want to run specific image only, run as following

``` shell
docker-compose start db
```

or 

```shell
docker-compose start wiki
```

Thereafter, access to [http://localhost:80/](http://localhost/) (or just http://localhost/ )

### Reference

- [Installation Documentation](https://docs.requarks.io/install/docker)
- [Github Repostory](https://github.com/requarks/wiki/)



