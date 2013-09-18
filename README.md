Coil Blog
=========

This is a sample blog using [Coil](https://github.com/badosu/coil)

Install
-------

Clone the repo and fetch dependencies:

    git clone https://github.com/badosu/coilblog
    cd coilblog && mix deps.get

Usage
-----

Edit `config.yml`.

Add an article: `mix post`

And run (binds to localhost:8080):

    mix run --no-halt

Deploy to Heroku:

    heroku create --buildpack "https://github.com/goshakkk/heroku-buildpack-elixir.git"
    git push heroku master

Customize
---------

### Articles

The content should be plain markdown.

Articles are stored in `articles/YYYY-mm-dd-article-title.md`

### Resources

Any asset stored on the `public/` folder will be served at the `/public` route

### Templates

Templates are stored in the `templates/` folder, and are embedded elixir files

See the [EEx docs](http://elixir-lang.org/docs/stable/EEx.html)

* layout.html.eex: The template in which all other templates are embedded
* index.html.eex: Renders the home page
* article.html.eex: Renders the article page
* archives.html.eex: Renders the archives page
* index.xml.eex: Renders the rss feed
