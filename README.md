# Setup


## Create project directory and clone module 13 files

### Clone module 13 github project
```bash
git clone git@github.com:kaw393939/module13_is601.git
```
### Create directory for assignment 13
```bash
mkdir assignment13

cd assignment13
```

### Copy module 13 files to assignment13 dir
```bash
cp -r ~/module13_is601/<file> .
```

### Open in VSCode
```bash
code .
```


## Initialization

### Set python version
```bash
pyenv local 3.10
```

### Create and activate venv
```bash
python3 -m venv venv

source venv/bin/activate
```

### Initialize repository
```bash
git init
```

### Set remote github repo
```bash
git remote add origin git@github.com:dbalicky/IS601_assignment13.git
```

### Initial commit and push
```bash
git add .

git commit -m 'initial commit'

git push --set-upstream origin main
```

## Installing dependencies 

### Update dependency versions in requirements.txt
```bash
cffi==1.17.1 --> 2.0.0
cryptography==44.0.0 --> 48.0.1
fastapi==0.115.8 --> 0.139.0
h11==0.14.0 --> 0.16.0
httpcore==1.0.7 --> 1.0.9
pyasn1==0.6.1 --> 0.6.4
python-jose==3.3.0 --> 3.5.0
python-multipart==0.0.20 --> 0.0.30
# remove starlette
typing-extensions==4.12.2 --> 4.13.2
urllib3==2.3.0 --> 2.7.0
```

```bash
pip install -r requirements.txt
```

# Docker setup

**Create Docker repo and add secret tokens to github**

### Check docker images currently running
```bash
docker compose ps
```

### Remove any running images
```bash
docker compose down -v
```

### Build new image
```bash
docker compose up --build
```

### Tag repo to docker
```bash
docker tag assignment13_web:latest dbal7/is601_assignment13:latest
```

### Push to docker repo
```bash
docker push dbal7/is601_assignment13:latest
```