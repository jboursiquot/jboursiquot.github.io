---
layout: post
title: "Transfering your bookmarks to Kippt"
description: "Don't leave behind all of your bookmarks from other services when you start using Kippt."
category: 
tags: [kippt, ruby, gem]
comments: true
published: true
---

If you're unfamiliar with [Kippt](http://kippt.com), it's a next-generation social
bookmarking service along the lines of Del.icio.us. 
It boasts a pretty neat user experience and I've found it to be
easy to use, enough so that I switched over from my long-time favorite,
[Instapaper](http://instapaper.com).

In order to not lose the hundreds of bookmarks I've horded over the
years, I exported them from Instapaper as a CSV and began pondering how
I was going to feed all of those links into Kippt. I certainly did not
want to do this manually and lose hours off of my life in doing so.
Instead I created a Ruby gem called
[bulkippt](https://rubygems.org/gems/bulkippt "bulkippt | rubygems.org")
that reads the CSV and transmits every bookmark to Kippt using their
[API](http://developers.kippt.com/ "Kippt Developer Documentation and
Resources"). Documentation for bulkippt is available on
[Github](https://github.com/jboursiquot/bulkippt
"jboursiquot/bulkippt").

But wait, there's more! While you can certainly use the gem in your web
apps, for me the fun was in using it on the command line through a
wrapper gem that I also created called
[bulkippt-cli](https://rubygems.org/gems/bulkippt-cli "bulkippt-cli |
rubygems.org").

To get started, first install the bulkippt-cli gem: 

{% highlight bash %} 
$ gem install bulkippt-cli
{% endhighlight %}

See the list of tasks you can call on the tool:

{% highlight bash %} 
$ bulkippt-cli help
{% endhighlight %}

Use the *submit* task with the path to your CSV and your Kippt creds and
the import will start. 

{% highlight bash %} 
$ bulkippt submit ~/path/to/my/bookmarks.csv -u kippt_username -t kippt_token
{% endhighlight %}

Speed of transmission will vary based on the size
of your CSV and condition of your connection to the internet.

Documentation for bulkippt-cli is available on
[Github](https://github.com/jboursiquot/bulkippt-cli
"jboursiquot/bulkippt-cli").
