# terminal-power

Because my memory sucks

## [AWS](https://aws.amazon.com/)

- `aws ecr get-login --no-include-email --region us-west-2`
- `$$(aws ecr get-login --no-include-email --region us-east-1)`

- `aws sts get-caller-identity --output text --query 'Account'`
- `aws sts get-caller-identity --output text --query 'Account' --profile=<some profile name>`

### [AWS S3](https://docs.aws.amazon.com/cli/latest/reference/s3/index.html)

- `aws s3 rb s3://bucket-name --force`
- `aws s3 ls s3://some-bucket/some-folder --recursive > ~/myFile.txt`
- `aws s3api list-objects-v2 --bucket="some-bucket" --prefix="SomeFolder/" --start-after="SomeFolder/SomeFile.txt" > ~/Desktop/s3-listing.json`

## [Brew](https://brew.sh/)

- `brew services list`
- `brew cleanup -n` and `brew cleanup`

## [Docker](https://www.docker.com/)

```shell
# Docker
docker context use rootless
docker exec -it <docker container/image name> /bin/bash
docker run --name <name> --net <network name> -p 0000:0000 -it <image name>

```

```shell
# Docker Compose (v2)
docker compose ls
docker compose ps
docker compose up
docker compose down
docker compose up -d
docker compose up -d <service name> --build
docker compose logs <service name> &2> ~/Desktop/logfile.log
docker compose logs <service name> > ~/Desktop/logfile.log
docker compose logs -f <some service name in the docker compose file>

```


## [DBDiff](https://github.com/DBDiff/DBDiff)

```yaml
# In your .dbdiff file

<arbitraryname>:
    user: dev
    password: password
    port: 3306
    host: 127.0.0.1
```

Note: Make sure you leave the named `server1` in the .dbdiff file, or the program chokes, even if you have other named DB's in the file.

- `./dbdiff --type=schema alliesDev.allies:alliesProd.allies`
- `./dbdiff --type=schema clarityDev.clarity:clarityProd.clarity`

### [Elastic Beanstalk](https://aws.amazon.com/documentation/elastic-beanstalk/)

- `eb printenv`
- `eb setenv key=variable`

## [Git](https://git-scm.com)

- `git apply --3way filename.patch`
- `git diff --cached > mypatch.patch`
- `git reset --hard HEAD^`
- `git status .`
- `git stash list`
- `git stash pop`
- `git stash drop` - Drops the "top" stash
- `git show -s --format=%ci`
- `git show -s --format=%ai`
- `git reset --soft HEAD~1`
- `git ls-tree -r master --name-only`
- `git clone --depth=1 <github repository>`
- `git remote add <somename> <some repo url>`
- `git pull <arbitrary name you gave the upstream> <branch in that upstream you want to pull from>`
- `git remote set-url --add --push origin <some repo url>`
- `git push --set-upstream origin master`
- `git rev-parse --short HEAD 2> /dev/null | sed "s/\(.*\)/\1/"`

## [Golang](https://go.dev/)

- `go env GOPATH`

## [Lando](https://lando.dev/) [Dev](https://github.com/lando/lando)

- `lando yarn start:dev`
- `lando ts-node /scripts/generate-typings.ts`
- `lando yarn run typeorm:migrate <migration name>`
- `lando yarn run typeorm:run`

## [Linux](https://linux.org/)

### [du (disk usage)](https://linux.die.net/man/1/du)

- `du -shc * | sort -h`

### [find](https://linux.die.net/man/1/find)

- `find . -type f -size +250M`

### [history](https://www.gnu.org/software/bash/manual/html_node/Bash-History-Builtins.html)

#### [Timestamp `history`]

- For BASH
  - `echo 'export HISTTIMEFORMAT="%d/%m/%y %T "' >> ~/.bashrc source ~/.bashrc` - https://askubuntu.com/a/391087
- [For ZSHRC](https://unix.stackexchange.com/a/103407/959)
  - `\history -E`
  - `fc -li 100`

### [ssh](https://www.ssh.com/ssh/)

- `ssh-keygen -R <hostname>` - Removes host ssh key so you can accept a new one

### [tail](https://linux.die.net/man/1/tail)

- `tail -c 25000 -f`

### [dos2unix](https://linux.die.net/man/1/dos2unix)

- `dos2unix -u --ascii somefile.txt`
- `dos2unix -ulb somefile.txt`
- `dos2unix -u -ul -b somefile.txt`

## [rsync](https://linux.die/net/man/1/rsync)

- `rsync --partial -rlvz --exclude='*/sites/default/files*' --size-only --ipv4 --progress -e 'ssh' user@somehost.com:/var/www/vhosts/somefolder/somesite .`

## Mac OSX

- `open myfile.txt`
- `base64 -d <<< dm9pbGE=` - Base64 Decode
- `echo -n "voila" | base64` - Echo string without newline character and pipe to base64 for encoding

## [Node]

- `node -p "require('./package.json').version"`

## [NodeJS Forever](https://github.com/foreverjs/forever)

- `forever -w app.js --watchIgnore node_modules`

## [NPM](https://npmjs.com)

- `npm i -g vue-cli` - Install vue-cli globally
- `npm version <some version | minor | major | patch>` - Have NPM increment the version number for you
- `npm publish --access=public --tag next --dry-run` - Dry run of publishing to the "next" dist-tag

## [Python](https://www.python.org/)

- `python`
- `python3`
- `pip install virtualenv`
- `pip3.11 install virtualenv`
- `virtualenv venv`
- `source venv/bin/activate`
- `python --version`
- `python3 -m http.server 8080 -d <where to start it at>`

## Rover

- `rover config auth`
- `rover graph fetch`
- `rover dev --url <url> --name <where to stitch it into the schema>`
- `rover subgraph introspect <url or local url>`

## [Serverless](https://serverless.com)

[Serverless Cheatsheet](https://serverless.com/framework/docs/providers/aws/guide/workflow/)

- `sls deploy`
- `sls package`
- `sls deploy list`
- `sls deploy function -f <function_name>`
- `sls deploy --force function --function app`
- `sls deploy --function-name=app --aws-s3-accelerate`
- `serverless create --template aws-nodejs --path tribute-serverless`
- `severless invoke local --function app`

## [Visual Studio Code]()

- `code -g myfile.txt:100`