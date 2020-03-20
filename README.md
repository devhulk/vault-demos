# vault-demos

## Run-Locally Instructions

Replace mount destination with mount point on your machine. 

### Clone Repo
```git clone https://github.com/devhulk/vault-demos.git```
### Move to vault config dir 
```cd vault-demos/vault/config```
### Get current dir...
```pwd```

Take output and paste in docker-compose file...
```
  vault:
    image: vault
    volumes: 
        - vault-config:$PASTE_HERE
```

Spin up project...
```
docker-compose up
```

Spin down project...
```
docker-compose down -v
```


## Pre-Steps

1. Enable Audit Device (file)

## Demo Steps

1. Enable AppRole Auth Method
2. Create Policy for App
3. Create AppRole w/ attached policy
4. Retreive RoleID and SecretID
5. Use RoleID and SecretID to login to vault
6. Use retrieved Client Token to read secret

## TODO
* Configure Audit Device (file)
* Troubleshoot AppRole reading secret with Client Token
* Add PGAdmin to docker-compose file
* Make sure PGAdmin can connect to Postgress instance
* Enable Postgres Database Secrets Engine
* Give AppRole access to Postgress DB SE path in app_policy.json
