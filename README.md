# Jekyll Template

This is a minimalist template project for jekyll that you can customise to suit your needs.  The idea is to get you up and running with analytics and comments and feedback as quick as possible.

I suggest you follow the [jekyll quick start instructions](http://jekyllrb.com/) to create your blog and then sync this template over it:

    gem install jekyll
    jekyll new my-awesome-site
    git clone https://github.com/krisb/jekyll-template.git
    rsync -av --progress jekyll-template/ my-awesome-site/ --exclude .git --exclude README.md
    cd my-awesome-site
    jekyll serve

## Markup

I prefer markdown, but you can use a number of supported markup formats.

## Pygments (code highlighting)

Assuming you have python installed with `easy_install` available:

    sudo easy_install Pygments

## Rake tasks

The following tasks are available (use `rake -T` to list them):

    rake build        # Build site with Jekyll
    rake check_links  # Check links for site already running on localhost:4000
    rake clean        # Clean up generated site
    rake deploy       # Build then deploy using rsync
    rake server       # Start server with --watch

The deploy task is simplistic and uses rsync to copy the generated site to your server.  You will need to replace the username, servername and path as appropriate.

## Configuration

There are a number of values in `_config.yml` to customise your site.  Change as appropriate.

Additionally, you can override and add additional values on a per page or post basis by adding variables into the front matter.  Support for the following is baked in:

* last_updated - will render updated date as well as original post date
* superseded - reference to a another post url

The following enhancements are baked in and enabled if you provide the configuration required.

* [Google Analytics](http://www.google.com/analytics) - web analytics using the [async](http://www.google.com/support/analytics/bin/answer.py?hl=en&answer=174090) script
* [Disqus](http://disqus.com/) - comments and feedback
* [Feedburner](http://feedburner.google.com/) - rss feeds
* [Github Ribbon](https://github.com/blog/273-github-ribbons) - fork me on github ribbon
