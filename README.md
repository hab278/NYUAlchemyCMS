Alchemy CMS Installation
========================

You can install Alchemy CMS by two ways-:
* Install as a standalone project
* Install into an existing Rails project

Install as a standalone project
-------------------------------
First install alchmey_cms gem then create a new project with alchemy
```
$ gem install alchemy_cms --pre
$ alchemy new nyu_library
```
Install into an existing Rails project
--------------------------------------
1. Add the Alchemy gem:
   Put this into your Gemfile:
   ```
   gem 'alchemy_cms', github: 'magiclabs/alchemy_cms', branch: 'master'
   ```
2. Update your bundle:
  ``` 
  $ bundle install
  ```

3. Set the authentication user

   You can use the Alchemy user model. Just add the following gem into  your Gemfile:
   ```
   gem 'alchemy-devise', '~> 2.0'
   ```
   Then run:
   ```
   $ bundle install
   $ bin/rake alchemy_devise:install:migrations
   ```
4. Install Alchemy into your app:

   After you set the user model you need to run the Alchemy install task:
   ```
   $ bin/rake alchemy:install
   ```
Now everything should be set up and you should be able to visit the Alchemy Dashboard at:
    http://localhost:3000/admin

* Use your custom path if you mounted Alchemy at something else then '/'
