<p align="center">
  <img src="https://cdn.rawgit.com/Navarra/website/6aabe0f6/public/assets/header.png" width="650">
</p>

[![Build Status](https://travis-ci.org/Navarra/website.svg?branch=master)](https://travis-ci.org/Navarra/website) [![Join the chat at https://gitter.im/Navarra/website](https://badges.gitter.im/Navarra/website.svg)](https://gitter.im/Navarra/website?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Register your player here to start your adventure.


[![Greenkeeper badge](https://badges.greenkeeper.io/Navarra/website.svg)](https://greenkeeper.io/)

---

First, create your `MySQL` database. Easy peasy. Call it `navarra`, I guess.

Secondly, in your terminal, make a new directory called `navarra` and type the following:

      $ git clone https://github.com/Navarra/website
      $ cp .env.example .env

Then, let's edit the `.env` file we just created from our last command (`cp`) and put in the database credentials.

Now, let's make the website. In your terminal, at `/navarra/website/`, type:

      $ composer install
      $ php artisan jwt:secret
      $ php artisan key:generate
      $ php artisan migrate
      $ php artisan config:cache
      $ npm install
      $ npm dev

Your website's CSS should now be compiled and your database's tables should now be created. Also, your secret JWT authentication key was created along with the Laravel application key.

Time to make your player! Let's serve up the website:

      $ php artisan serve

Now go to `https://localhost:8000` and register your player account. You are all set!

### Caution

This is NOT needed to run the game locally. When Navarra runs locally, it creates a local player.