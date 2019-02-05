---
layout: post
date:   2019-02-05 07:00:00 +0900
categories: blogs
---

This is my current docker command for jekyll.

~~~shell

@echo off
set JEKYLL_VERSION=3.8
docker run --rm ^
  -p 80:4000 ^
  --volume="%CD%/trueonot.github.io:/srv/jekyll" ^
  --volume="%CD%/vendor/bundle:/usr/local/bundle" ^
  -it jekyll/builder:%JEKYLL_VERSION% ^
  bash

~~~
then I execute the jekyll server like below.
~~~shell

  bash-4.4# jekyll serve --force_polling

~~~

--force_polling : this option is used for polling. jekyll has default setting for auto-generation when I change anyhing, however, as you see in above I connect it to windows file system. Because of that change didnt' notified to jekyll server. 

Because I am not used to set docker environment and jekyll neither. I have to do manually when I encounter any problems. also sometimes I have to reboot jekyll server when I changing the _config.yml.

In addition to, I also modified the template for switch url. since this theme is developed to swtich localhost and github manually. I found that default configuration from jekyll is enough to test jekyll in localhost.

~~~yml

  # Site settings
  url: https://trueonot.github.io/
  baseurl: /

~~~
It works well for now. also I add syntax highlighter. let's see on github. 

**trueonot:follow your heart's, it's right way**