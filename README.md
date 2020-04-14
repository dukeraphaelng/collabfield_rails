# How to build a Rails app without breaking everything



### Step 1: Initializing a new project

- rails new collabfield --database=postgresql
- cd collabfield
- bundle install
  - bundle update
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
- 