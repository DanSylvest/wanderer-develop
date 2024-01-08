# wanderer-develop

1. clone in this folder this
```bash

git clone https://github.com/DanSylvest/wanderer-client.git

# 2. clone in this folder this
git clone https://github.com/DanSylvest/wanderer-server.git

# 3. clone here eve-route-builder
git clone https://github.com/DanSylvest/eve-route-builder.git

# 4. clone here zkb-kills-provider
git clone https://github.com/DanSylvest/zkb-kills-provider.git

```
2. visit [developers](https://developers.eveonline.com/applications) site.
   1. make your own application
   2. add this permissions
    ```sh
    "esi-location.read_location.v1"
    "esi-location.read_ship_type.v1"
    "esi-location.read_online.v1"
    "esi-ui.write_waypoint.v1"
    "esi-search.search_structures.v1"
    ```
3. set **EVE_CLIENT_ID** and **EVE_SECRET_KEY** in file _**.env.local**_
4. download docker application from [official site](https://www.docker.com/)
5. after install open terminal in this folder via WebStorm/VSCode/Terminal... etc.

###
#### Next work with docker, after it started
```sh
# Build images 
docker-compose --env-file=.env.local build

# after build 
docker-compose --env-file=.env.local up
```

###
#### If you wanna clear all docker files
```bash
# after it you need go to project folders and delete lock_files:
# wanderer-client/lockfile_client, wanderer-server/lockfile_server
docker-compose --env-file=.env.local down --remove-orphans
```

## Debug 
#### You can use this link to open debug window http://localhost:9229/json for server
#### or go here chrome://inspect/#devices

### All files hot reloading on changes, not necessary to restart docker everytime
