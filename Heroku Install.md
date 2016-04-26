## Specify a buildpack for a rust project

$> heroku create --buildpack https://github.com/emk/heroku-buildpack-rust.git
created app calm-plains-3817
$> heroku git:remote -a calm-plains-3817
$> git remote show
heroku
origin
$>git remote show heroku
* remote heroku
  Fetch URL: https://git.heroku.com/calm-plains-3817.git
  Push  URL: https://git.heroku.com/calm-plains-3817.git
  
$heroku apps:rename iron-curtain --app calm-plains-3817
Renaming calm-plains-3817 to iron-curtain... done
https://iron-curtain.herokuapp.com/ | https://git.heroku.com/iron-curtain.git
Git remote heroku updated

git remote show heroku
* remote heroku
  Fetch URL: https://git.heroku.com/iron-curtain.git
  Push  URL: https://git.heroku.com/iron-curtain.git
  
## To switch to ssh git 

``` 

git remote set-url heroku git@heroku.com:iron-curtain.git
git remote set-url origin git@gitlab.com:ivanceras/curtain.git
```


## Don't forget to set rust version in RustConfig file

```
cat RustConfig
VERSION="1.2.0"

```
## Configure the environment variables
DATABASE_URL : postgres://atperknxxnjadk:jpasCIjuPd3MW48DUnb579-imU@ec2-23-21-140-156.compute-1.amazonaws.com:5432/dd2fbo2kj0q9l

PORT : 80

##Deployed to 
https://iron-curtain.herokuapp.com