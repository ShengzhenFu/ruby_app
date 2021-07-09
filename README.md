# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version
## install ruby on Manjaro
```
sudo pacman -S ruby
cat << EOF >> ~/.zshrc
export GEM_HOME="$(ruby -e 'puts Gem.user_dir')"
export PATH="$PATH:$GEM_HOME/bin"
EOF
source ~/.zshrc
gem install rails
gem install rake
gem install bundle

ruby -v
rails -v
rake -v
bundle -v
```
* System dependencies

* Configuration
## install postgresql on Manjaro
```
sudo pacman -S postgresql postgis
sudo su postgres -l # or sudo -u postgres -i
initdb --locale $LANG -E UTF8 -D '/var/lib/postgres/data/'
sudo systemctl enable --now postgresql.service
psql --version
```
psql commands: https://www.postgresqltutorial.com/psql-commands/
* Database creation
create role username superuser;
create user username;
alter role username with login;
create database ruby_app_development;
* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
