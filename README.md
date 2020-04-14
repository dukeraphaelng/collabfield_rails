# How to build a Rails app without breaking everything



*Author: Duke Nguyen*

*Git Repository: https://github.com/dukeraphaelng/collabfield_rails*

This is a step-by-step instruction guide on how to build a rails app improving from the original freeCodeCamp article linked [here](https://www.freecodecamp.org/news/lets-create-an-intermediate-level-ruby-on-rails-application-d7c6e997c63f/)



### Step 1: Initializing a new project

- rails new collabfield --database=postgresql
- cd collabfield
- bundle install
  - bundle update
  - gem install bundler:2.1.4
    *if gem bundler installer is older than current gemfile's bundle version* 
- rails db:create
- rails db:migrate
- pg_ctl -D /usr/local/var/postgres start
  Start postgresql manually
- git init
- git add .
- git commit -m 'First commit'
- git remote add origin 'link_to_remote'
- git push origin master
- rails s
- *Go to* localhost:3000



### Step 2: Generating pages controller

- rails g / generate controller pages