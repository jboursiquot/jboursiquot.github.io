---
layout: post
title: "Bulk Mail Dispatching from the Command Line"
description: "Recently I was in need of sending a large quantity of
emails to a pre-defined list of users. I wanted to do it on the command
line–where I do most of my work–but unfortunately couldn’t find anything
suitable for my needs so I created one: Maildis."
category: 
tags: [mail, ruby, gem, cli]
comments: true
published: true
---

Maildis supports HTML and plain text templates with merge tags and CSVs for
specifying recipients. It relies on SMTP information you provide through
your own configuration file. Subject, sender, path to CSV and path to
the templates are all configurable through YAML.

Maildis is distributed as a Ruby Gem and can be found on 
[rubygems.org](https://rubygems.org/gems/maildis "maildis | rubygems.org"). 
Usage and documentation are available on
[GitHub](https://github.com/jboursiquot/maildis "jboursiquot/maildis"). 
