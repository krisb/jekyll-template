# Jekyll Template

This is a template project for jekyll that you can clone and customise to suit your needs.  Its quite opinionated in what it provides, the idea is to get you up and running with feed support, analytics and comments and feedback.  This is meant for a standalone blog, not for [github pages](http://pages.github.com/)

Please don't fork otherwise I'll see lots of noise on the fork queue that are your customisation for your blog.  I suggest you create a repo on github (public or private, its up to you) and do the following assuming the new repo is available at `https://github.com/username/reponame`:

    git clone https://github.com/krisb/jekyll-template.git mysite
    cd mysite
    rm -rf .git
    git init
    git commit -m 'initial template based on https://github.com/krisb/jekyll-template'
    git remote add origin git@github.com:username/reponame.git
    git push origin master

The following sections detail how to set up and use the template.  The commands are known to work on my macbook, YRMV.

## Ruby 1.9.2 via RVM

I recommend that you install rvm and set everything up using that.

    bash < <( curl http://rvm.beginrescueend.com/releases/rvm-install-head )

Follow the instructions to add the necessary lines in `.bashrc`, e.g.

    # RVM
    if [[ -s "$HOME/.rvm/scripts/rvm" ]] ; then
      source "$HOME/.rvm/scripts/rvm"
    fi

Now source `.bashrc` (you don't need to do this normally as it runs on login, it is just to update the current term window)

    source ~/.bashrc

You can then install and use ruby 1.9.2:

    rvm install 1.9.2
    rvm use 1.9.2

## Gems

Run the following to install the necessary gems:

    gem install jekyll rdiscount compass

## Markup

I prefer markdown, but you can use a number of supported markup formats.

## Stylesheets

I recommend that you use compass, see http://compass-style.org/.  I've included the scss for the syntax highlighting in `_sass/mixins/_syntax.scss`.

## Google Analytics

Uses the async script.  Replace `UA-XXXXX-X` with your id in `_layouts/default.html`.

See http://www.google.com/support/analytics/bin/answer.py?hl=en&answer=174090 for the details if you are interested.

## Disqus comments

Replace `disqusid` with your id once you sign up in 2 place in `_layouts/post.html`.

## Feedburner RSS

Replace `feedburnerid` with your id in `_layouts/default.html`

## Rake deploy task

There is a simple deploy task using rsync if you need it.  You will need to replace the username, servername and path as appropriate.

## Pygments (code highlighting)

Assuming you have python installed with easy_install available:

    sudo easy_install Pygments

## Other things to replace

There are a number of values in `_config.yml` to customise your site.  Change as appropriate.
