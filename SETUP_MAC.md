---
layout: page
---

# Getting started

Ensure you have homebrew setup and ready. Then install some deps:

```
$ brew update
$ brew install coreutils
```

Please use RVM for easy ruby version management, and for this repo use
ruby-2.2.5. Then install bundler, and let bundler setup the
remaining deps.

```
$ rvm install ruby-2.2.5
$ gem install bundler
$ bundle
```

After bundling, you should now be able to serve the pages:

```
jekyll serve
```

Then use your browser to visit, [http://127.0.0.1:4000/](http://127.0.0.1:4000/)
