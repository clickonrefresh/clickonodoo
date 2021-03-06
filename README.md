![image](https://user-images.githubusercontent.com/72121107/114523314-789a0100-9c44-11eb-996a-47d8224635c7.png)

# Clickonodoo

by clickonrefresh

[Join My Odoo Discord Community](https://discord.gg/46kKJ5VeHt)

## Odoo with Open HRMS and Nginx Proxy Manager

### [ghcr.io/clickonrefresh/clickonodoo](https://github.com/clickonrefresh/clickonodoo/pkgs/container/clickonodoo)

Customised Odoo ce with Open HRMS available for install, Python Pandas preinstalled.

Before installing third party modules, please see their relative dependency modules which must be installed prior to 3rd party module install.

---

# Using this repo
In Apps you will find the docker compose file along with odoo.conf and any addons. These are the files required to run Odoo.

### Navigate into Apps/ and your desired Odoo version or Nginx and run:

```
docker compose up -d
```

This will pull the relative odoo version image from ghcr.io/clickonrefresh/clickonodoo and configure volumes, port mapping and configure postgresql.



# Install.sh will install docker, docker compose and some other prerequisites:
comment out the lines for nodejs install if you do not intend to use odoo for development


```
bash install.sh 
```





<!-- # How to update this image via Dockerfile

Make sure your Dockerfile, entrypoint.sh, odoo.conf and wait-for-psql.py files are up to date with the latest (official Odoo docker repo)[https://github.com/odoo/docker]

## The following customizations must be included in the following files for customization:

### Dockerfile

```
python3-pandas \
```

...
....
...

# How to use this repo image

## Login to your respective container registry

`docker login <registry url>`

## Change directory into the Dockerfile location

`cd DockerBuild/14.0/`

## Build the image from the Dockerfile

`docker build -t ghcr.io/clickonrefresh/clickonodoo .`

### where -t is to tag the image, default is latest or main depending on container registry.

### the period at the end of the line is to specify that the Dockerfile be built from the current file path.

## Build the image with a different tag

`docker build -t ghcr.io/clickonrefresh/clickonodoo:dev .`
`docker build -t ghcr.io/clickonrefresh/clickonodoo:staging .`
`docker build -t ghcr.io/clickonrefresh/clickonodoo:14.0 .`

#### and so on

## Finally push your changes to the registry

`docker push ghcr.io/clickonrefresh/clickonodoo`
fails with bad credential setup

# How to scaffold a new app using docker

## Enter the container

`docker exec -u root -it <containerID> /bin/bash`

## Inside the container, run

`/usr/bin/odoo scaffold <yourappname> /mnt/extra-addons`

### If you have used this repo to create an app then your newly creted app will appear in the project folders under odo/addons. This external path has been mapped to /mnt/extra-addons inside the container.

## Now change the file permissions to allow editing

`sudo chown -R $USER:$USER <yourappname>` -->

<!-- https://docs.docker.com/engine/reference/commandline/login/#credentials-store -->

