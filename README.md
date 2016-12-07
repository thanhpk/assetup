# assetup
Static assets upload and download plugin

# Development flow

### Run project
```sh
assetup $ composex docker-compose.dev.yml > docker-compose.yml
assetup $ docker-compose build
assetup $ docker-compose up
```
### Publish project
```
assetup $ composex docker-compose.prod.yml > docker-compose.yml
assetup $ docker-compose build
assetup $ docker push thanhpk/asset
```

### Change config or source code in deps
```sh
assetup/deps/componentA $ composex docker-compose.prod.yml > docker-compose.yml
assetup/deps/componentA $ docker-compose build
assetup/deps/composentA $ cd ../..
assetup $ docker-compose rm
assetup $ docker-compose up # dont have to rebuild whole project
```

### Change config or source code in project
It refresh automatically, you don't have to do anything.
