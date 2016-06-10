Sample Elixir Plug application
======================================

Running Locally
---------------

First, you need to have a working Elixir environment:

http://elixir-lang.org/install.html

You must specify the listening port using the `PORT` environment variable

### Install dependencies
```bash
mix deps.get
```

### Compile project

```bash
mix compile
```

### Execute
```bash
mix run --no-halt
```

Deploying on Scalingo
---------------------

Create an application on https://scalingo.com, then:

```
git remote add scalingo git@scalingo.com:<name_of_your_app>.git
```
Set the `BUILDPACK_URL` environement variable to `https://github.com/HashNuke/heroku-buildpack-elixir.git`.

You can do it using the web dashboard, select your application, go to the `Environment` tab and add :
```
BUILDPACK_URL=https://github.com/HashNuke/heroku-buildpack-elixir.git
```

If you want to do it using the scalingo cli interface juste type :
```sh
scalingo -a <name_of_your_app> env-set BUILDPACK_URL=https://github.com/HashNuke/heroku-buildpack-elixir.git
```

Next you'll need to push it to scalingo :
```sh
git push scalingo master
```

And that's it!

The application is running at this url: http://sample-elixir-plug.scalingo.io

Deploy in one click
-------------------

[![Deploy to Scalingo](https://cdn.scalingo.com/deploy/button.svg)](https://my.scalingo.com/deploy)

Links
-----
http://elixir-lang.org/
https://github.com/elixir-lang/plug
