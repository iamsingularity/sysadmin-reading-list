# sysadmin-reading-list

[![Build Status](https://travis-ci.org/unixorn/sysadmin-reading-list.png)](https://travis-ci.org/unixorn/sysadmin-reading-list)

A reading list for the larval stage sysadmin. This list is focused on the UNIX family of OSes.

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Books to Read](#books-to-read)
- [Languages](#languages)
  - [Bash](#bash)
  - [Ruby](#ruby)
  - [Python](#python)
    - [Tutorial](#tutorials-@-python)
    - [Sysadmin](#python-&-sysadmin)
    - [Deployment Utils](#python-&-deployment)
- [Tools](#tools)
  - [Cloud](#cloud)
    - [AWS](#aws)
  - [Configuration Management](#configuration-management)
  - [Regular Expressions](#regular-expressions)
  - [Sed & Awk](#sed-&-awk)
  - [Source control](#source-control)
    - [Git](#git)
  - [SSH](#ssh)
  - [Text Editors:](#text-editors)
    - [Vim](#vim)
    - [Emacs](#emacs)
    - [Visual Editors and IDEs](#visual-editors-and-ides)
- [Blogs and Podcasts](#blogs-and-podcasts)
- [Other Resources](#other-resources)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

So you've got your first sysadmin job. Congratulations, it's going to be an interesting ride.

## Books to Read

* [Effective DevOps](http://shop.oreilly.com/product/0636920039846.do) - A practical guide for creating affinity among teams and promoting efficient tool usage in your company.
* [Site Reliability Engineering](http://shop.oreilly.com/product/0636920041528.do) - How Google Runs Production Systems.
* [The Phoenix Project](http://smile.amazon.com/Phoenix-Project-DevOps-Helping-Business-ebook/dp/B00AZRBLHO) - know why your projects are important to the business
* [Time Management for System Administrators](http://smile.amazon.com/Management-System-Administrators-Thomas-Limoncelli/dp/0596007833), by Tom Limoncelli. You're going to be pulled in a dozen different directions, if you can't manage your time you're going to suffer.
* [UNIX-Linux-System-Administration-Handbook](http://smile.amazon.com/UNIX-Linux-System-Administration-Handbook/dp/0131480057) by Nemeth is a great book, this book is targeted to larger system deployments and real world large systems.

## Languages

### Bash

Every sysadmin needs to know Bash.

* [Bash Pitfalls](http://mywiki.wooledge.org/BashPitfalls) - Greg Wooledge has a great list of unpleasant surprises in Bash
* [Learning the Bash Shell](http://shop.oreilly.com/product/9780596009656.do) - hard to go wrong with an O'Reilly reference on anything, really.
* Google's [Shell Style Guide](https://google.github.io/styleguide/shell.xml) lists what Google's developers consider best practices for bash scripts.
* [shellcheck](http://shellcheck.net) is a lint for bash. It'll help you find unused variables, deprecated syntax and other things that make your bash scripts less stable. You can install it with `apt-get`, `brew`, `cabal`, or `yum`.

### Ruby

If you're in a Ruby shop, you'll want these:

* [Ruby Best Practices](http://shop.oreilly.com/product/9780596523015.do)
* [The Ruby Programming Language](http://shop.oreilly.com/product/9780596516178.do)

### Python

As of Python, compared to bash, you will love it's higher support towards string manipulation and system infrastructure.

A couple of places to go into as training would be:

#### Tutorials @ Python

* [Learn Python the Hard Way](http://learnpythonthehardway.org/book/), a rather comprehensive tutorial covering many aspects of the language.
* [Programming Python](http://shop.oreilly.com/product/9780596158118.do), a well-written O'Reilly book, short and concise. 

#### Python & Sysadmin

* [Practical Python for Sysadmins](http://macadmins.psu.edu/wp-content/uploads/sites/1567/2013/06/psumacconf2013-practical-python-for-mac-admins.pdf), an awesome transition course from Bash to Python (full highlights).
* [General Data](http://docs.python-guide.org/en/latest/scenarios/admin/), a neat place to see usage and examples of Python and not only.
* [WSGI - Web Server Gateway Interface](http://uwsgi-docs.readthedocs.io/en/latest/WSGIquickstart.html), the Python implementation of web servers.

#### Python & Deployment Utils

* [WSGI + Gunicorn tutorial](https://www.digitalocean.com/community/tutorials/how-to-deploy-python-wsgi-apps-using-gunicorn-http-server-behind-nginx)
* [WSGI + Flask tutorial](https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
* [WSGI + Pyramid tutorial](https://www.digitalocean.com/community/tutorials/how-to-deploy-pyramid-based-python-wsgi-web-applications)

Tools

### Cloud

#### AWS

* [AWSCli](https://github.com/aws/aws-cli) provides a unified command line interface to Amazon Web Services. Wean yourself off of the webui if you want to be truly productive
* [S3cmd](http://s3tools.org/s3cmd) is a free command line tool and client for uploading, retrieving and managing data in Amazon S3 and other cloud storage service providers that use the S3 protocol, such as Google Cloud Storage or DreamHost DreamObjects.
* [og-aws](https://github.com/open-guides/og-aws) is an excellent resource to AWS written by and for engineers who use AWS extensively.

### Configuration Management

Quite simply, if you aren't using configuration management, you're doing it wrong.

You don't want to manually configure any servers - no matter how hard you try, they won't end up truly identical and having meat typing in commands takes far too long per server, doesn't scale, and the manual labor will discourage you from standing up new VMs for testing.

There are several good options:

* [Ansible](http://www.ansible.com/) is designed to be minimal in nature, consistent, secure, and highly reliable. Was recently purchased by Red Hat.
* [Chef](http://www.opscode.com/chef/) is written in Ruby and Erlang and uses a Ruby DSL to describe system configuration
* [Puppet](http://puppetlabs.com/) makes it easy to automate the provisioning, configuration and ongoing management of your machines and the software running on them. Make rapid, repeatable changes and automatically enforce the consistency of systems and devices – across physical and virtual machines, on premise or in the cloud.
* [Salt](http://www.saltstack.com/) orchestrates the build and ongoing management of your infrastructure.

### Regular Expressions

Among the many places you're going to find regexes very useful for is handling logs. When you have a multi-gigabyte logfile, it's a lot less painful to look at just the entries generated by the service that you got alerted about.

* [Introducing Regular Expressions](http://shop.oreilly.com/product/0636920012337.do)
* [Regular Expressions Cookbook](http://shop.oreilly.com/product/0636920023630.do)

### Sed & Awk

* [sed and awk Pocket Reference](http://shop.oreilly.com/product/9780596003524.do) presents a concise summary of regular expressions and pattern matching, and summaries of sed and awk and how to use them to edit files and convert data from one format to another.

### Source control

No matter what source control you use (git, hg, perforce, whatever), you're going to have to write commit messages. Make them good. Explain _why_ you made the change, not just _what_ you changed. And no, the diff is not an explanation.

Good commit messages help the rest of your team understand what you're trying to do and make it easier for them to find logic errors in your pull requests - the code may be technically correct, but if they understand what you're _trying_ to do, they can see when your code isn't actually doing what you want it to.

Here are a few articles that while focused on git apply to any system you're using:

* [5 Useful Tips for a Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message) is another good article on writing commit messages.
* [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html)
* [Writing Good Commit Messages](http://chris.beams.io/posts/git-commit/) is a good article on writing coherent commit messages

#### Git

Whether or not your shop uses git internally, you're going to end up needing to use it for the many useful things on GitHub.

* [19 Git Tips for Everyday Use](http://www.alexkras.com/19-git-tips-for-everyday-use/) - a good set of starter tips for using git
* [git-flight-rules](https://github.com/k88hudson/git-flight-rules) is Kate Hudson's guide to using Git in specific situations.
* [git-tips/tips](https://github.com/git-tips/tips) is a collection of git tips
* [Pro Git](https://git-scm.com/book/en/v2) by Scott Chacon and Ben Straub is a great overall resource for git.
* [Why the Heck is Git so Hard? The Places Model](http://merrigrove.blogspot.com/2014/02/why-heck-is-git-so-hard-places-model-ok.html) - an article about moving from SVN/CVS to git.

### SSH

* [SSH, The Secure Shell: The Definitive Guide, 2nd Edition](http://shop.oreilly.com/product/9780596008956.do)

### Text Editors:

Don't get involved in the Editor Wars.  Just.  Don't.  Your choice of tool does not need defending.  Nor does anyone else's choice.

However, you should care about your tools.  You should be able to use them efficiently.

#### Vim

Vim is a reality of life for SysAdmins.  It is the one editor you can be sure is installed in even the most minimal install. You must be able to do at least basic edits with it.  You don't need to love it, but you will have to use it.

* [Damian Conway, "More Instantly Better Vim" - OSCON 2013](https://www.youtube.com/watch?v=aHm36-na4-4)
* [vi and Vim Editors Pocket Reference, 2nd Edition](http://shop.oreilly.com/product/0636920010913.do)

#### Emacs

Many people like Emacs.  You might be one of them.  Don't be afraid to try it out.

#### Visual Editors and IDEs

Use tools with which you are productive.  If you want to use a GUI Text Editor or IDE, don't let anyone give you a hard time about that.

There are GUI versions of vim and emacs that have ardent followers.

[Atom](https://atom.io/) is a fairly new editor with significant traction and plugin ecosystem.
[Sublime Text](http://sublimetext.com) is another editor with an extensive plugin ecosystem and arguably one of the inspirations for Atom.

## Blogs and Podcasts

* [Arrested Devops](https://www.arresteddevops.com/) is hosted by Matt Stratton, Trevor Hess, and Bridget Kromhout. ADO is the podcast that helps you achieve understanding, develop good practices, and operate your team and organization for maximum DevOps awesomeness.
* [Code as Craft](http://codeascraft.com/) is Etsy's ops blog and is full of well written examples of dealing with real-world problems at scale.
* [Julia Evans' Blog](http://jvns.ca/) - Julia writes a great blog where she'll dive into interesting topics and explain them clearly.
* [Kitchen Soap](http://www.kitchensoap.com/) - John Alspaw is the CTO at Etsy and writes a great blog about web operations and operating at scale and other things that are interesting to ops types.

## Other Resources

* [awesome-sysadmin](https://github.com/n1trux/awesome-sysadmin) - A curated list of awesome open-source sysadmin resources.
