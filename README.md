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