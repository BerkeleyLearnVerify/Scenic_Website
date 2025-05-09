# scenic-lang.org

This repository contains the source for the [scenic-lang.org](https://scenic-lang.org) web site.

It does not contain the source for the [scenic-lang.readthedocs.io](https://scenic-lang.readthedocs.io/en/latest/index.html) documentation. You can visit the [Scenic repository](https://github.com/BerkeleyLearnVerify/Scenic) if you are interested in contributing to the Scenic documentation site.

The repository for Scenic itself is https://github.com/BerkeleyLearnVerify/Scenic.

## Dependencies

To build the site you can either use [Compose](https://github.com/docker/compose) or [Bundler](https://github.com/bundler/bundler). Compose is a good option if you are just getting
started and want something simple. If you are already familiar with the Ruby ecosystem then Bundler
might be the most comfortable for you.

Either way the site is built with [Jekyll](https://github.com/jekyll/jekyll) and is typeset mostly in
Markdown.

## Building the site
Make sure you are in the root directory of the cloned repository.
### With `Docker Compose`:

You need to have [Docker Engine](https://docs.docker.com/engine/) and [Docker Compose](https://docs.docker.com/compose/) installed on your machine.
Under macOS (Intel or Apple silicon), instead of installing [Docker Desktop](https://docs.docker.com/desktop/) you can also use [HomeBrew](https://brew.sh/) with [Colima](https://github.com/abiosoft/colima): `brew install colima docker docker-compose`.  
UID and GID environment variables are needed to avoid docker from writing files as root in your directory.
By default, docker-compose will use the file docker-compose.yml which will build the website and serve it on 0.0.0.0:4000 .
If you just need to build the website, add ```-f docker-compose_build-only.yml```

```
env UID="$(id -u)" GID="$(id -g)" docker-compose up
```

The generated site is available at `http://localhost:4000/Scenic_Website/`.

When the website dependencies change (the content of the `Gemfile`),
you have to re-build the Docker image:

```
env UID="$(id -u)" GID="$(id -g)" docker-compose up --build
```

If you have problems with the Docker image or want to force the rebuild of the Docker image:
```
env UID="$(id -u)" GID="$(id -g)" docker-compose build --no-cache
```



### With Bundler:

Install bundler first:

```
sudo gem install bundler
```

Then:

```
bundle install
bundle exec jekyll serve --incremental
```

## Viewing the site

Regardless of your method of running Jekyll, the generated site is available at `http://localhost:4000`.

## Editing the Site

### YAML Front Matter

The "YAML Front Matter" is nothing more than the header on each page that you intend for Jekyll to parse. It contains information such as the name of the HTML template (layout) chosen for the specific document, and the title of the document. An example YAML front matter might look like:

    ---
    layout: page
    title: My page title
    ---

You can use these fields in the YAML front matter later in your document. For example, to make a header with the title of the document, in Markdown you would write:

    ---
    layout: page
    title: My page title
    ---

    # {{ page.title }}

    Body text here...

`# {{ page.title }}` would be rendered in HTML as, `<h1>My page title</h1>`.

### Recommended Markdown Editor

[Visual Studio Code](https://github.com/Microsoft/vscode) has great support for Scenic, Git, and Markdown.

### Linking to internal pages

The least error-prone way to make links is to use this format: `[link text]({{ site.baseurl }}/path/to/page/page.html)`

`{{ site.baseurl }}` is a site-wide variable that represents the root directory of the static site. So, to display the Scenic logo image you can simply write: `![Img alt text]({{ site.baseurl }}/resources/img/scenic-logo.png)`

### Permalinks

We try to follow a [pretty permalink](https://jekyllrb.com/docs/permalinks/) style, so that any generated page will have a link finishing in a slash character (`/`). This will tell Jekyll to build that particular page as an `index.html` inside a folder with a name as specified in the provided permalink. i.e.: if a page has a permalink as follows:

`permalink: /what-is-scenic/`

This will tell Jekyll to create a `what-is-scenic` directory, with an `index.html` file inside. Links to this page will refer to the `{{site.baseurl}}/what-is-scenic/`.

### Custom collections and data

Every [collection](https://jekyllrb.com/docs/collections/) is a directory starting with an underscore character (`_`), containing a Markdown file for each member of the collection. These Markdown files start with a YAML front matter containing the data for this item, and can optionally contain markdown text to be rendered as html.

Right now there are no collections being rendered as specific pages in the site. They are only consumed internally as data. In the future this can be changed by specifying the global `output: true` variable in the `_config.yml` custom collections section. You will also need to specify a layout by using the `defaults` settings in the `_config.yml` file. i.e.:

```
defaults:
  - scope:
      path: ""
      type: collection_name
    values:
      layout: layout_name
```

To access data from a custom collection refer to `site.<collection-name>`. The collection's name will be the name of it's directory without the underscore character. i.e.: to access the data inside `_downloads`, use `site.downloads`.

Some of our data has been modelled as YAML files inside the `_data` folder. We generally do this for data that is used throughout the whole site. For example we do this for the navigation bar links.

### Credits

Credits to [scala-lang](https://github.com/scala/scala-lang) for the website layout. Scala is licensed under the [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
