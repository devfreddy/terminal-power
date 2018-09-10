# terminal-power
Because my memory sucks

## [AWS]()

- `aws ecr get-login --no-include-email --region us-west-2`
- `$$(aws ecr get-login --no-include-email --region us-east-1)`

## [Brew](https://brew.sh/)

- `brew services list`

## [Git](https://git-scm.com)

- `git apply --3way filename.patch`
- `git diff --cached > mypatch.patch`
- `git reset --hard HEAD^`
- `git status .`
- `git stash list`
- `git stash pop`
- `git show -s --format=%ci`
- `git show -s --format=%ai`
- `git reset --soft HEAD~1`
- `git ls-tree -r master --name-only`
- `git clone --depth=1 <github repository>`
- `git remote add origin <some repo url>`
- `git remote set-url --add --push origin <some repo url>`
- `git push --set-upstream origin master`
- `git rev-parse --short HEAD 2> /dev/null | sed "s/\(.*\)/\1/"`

## [Lando](https://github.com/lando/lando)

## [Linux]()

### [find](https://linux.die.net/man/1/find)

- `find . -type f -size +250M`

### [tail](https://linux.die.net/man/1/tail)

- `tail -c 25000 -f`

### [dos2unix](https://linux.die.net/man/1/dos2unix)
- `dos2unix -u --ascii somefile.txt`
- `dos2unix -ulb somefile.txt`
- `dos2unix -u -ul -b somefile.txt`

## Mac OSX

- `open myfile.txt`

## [NodeJS Forever](https://github.com/foreverjs/forever)
- `forever -w app.js --watchIgnore node_modules`

## [Serverless](https://serverless.com)

[Serverless Cheatsheet](https://serverless.com/framework/docs/providers/aws/guide/workflow/)

- `sls deploy`
- `sls package`
- `sls deploy list`
- `sls deploy function -f <function_name>`
- `sls deploy --force function --function app`
- `sls deploy --function-name=app --aws-s3-accelerate`
- `serverless create --template aws-nodejs --path tribute-serverless`

## [Visual Studio Code]()

- `code -g myfile.txt:100`