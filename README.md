## Grav CMS Under Docker
Installation
## Docker
This document assumes that you have docker installed and that you have git installed.
clone this repository into the file system you wish to edit the application code

docker compose build

This should download and create the requisite docker images and mount points

docker compose run -d

This should run the containers on the localhost at port 80

