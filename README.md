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
- rails g / generate controller pages



### Step 2: Adding and Configuring Bootstrap

- Check the latest bootstrap version
  https://github.com/twbs/bootstrap-rubygem

  - gem 'boostrap', '>= 4.0.0'

  - bundle install

  - @import "bootstrap";

  - remove:

    - ```scss
      *= require_self
      *= require_tree .
      ```

  - ```bash
    gem 'jquery-rails'
    ```

  - ```
    //= require jquery3
    //= require popper
    //= require bootstrap-sprockets
    ```

  - ```rb
    <%= render 'layouts/navigation' %>
    ```

    Only add the following code after putting itmes in partials/layout/ otherwise return errors.

  - ```scss
    @import "partials/layout/*";
    ```

  - Add <div class="container"> to link_to



### Step 3: Configuring Devise

- ```
  gem 'devise'
  ```

  ```bash
  rails generate devise:install
  ```

- ```bash
  rails generate devise User
  ```

- Restart server, otherwise returns undefined method error

